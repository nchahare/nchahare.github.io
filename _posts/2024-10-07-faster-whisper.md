---
title: "Transcribing audio with Faster whisper"
author: Nimesh Chahare
layout: post
date: 2024-07-30
tags: resources
---

# How to use faster-whisper

It is incredibly easy to install and run. After exploring many options both online and offline, I found this app that allows you to transcribe audio with fairly good accuracy. The time it takes to transcribe is roughly the same as the duration of the audio.

Additionally, it is free, unlike OpenAI Whisper, which requires payment. Here, you only spend time on computation, and I am fine with that.

Having a GPU might have been beneficial, but it is not feasible for me due to my laptop. It's unfortunate.

# Installation

Fairly straightforward. Just follow the instructions from the [github repo](https://github.com/SYSTRAN/faster-whisper). It is just start your own virtual environment and run pip.

```python
python -m venv myenv  # Create a new virtual environment
.\myenv\bin\activate  # Activate the virtual environment
pip install faster-whisper # install github
```

## Usage

I copy pasted following script to a jupyter notebook

```python
from faster_whisper import WhisperModel

model_size = "distil-large-v3"

model = WhisperModel(model_size, device="cpu", compute_type="int8")

segments, info = model.transcribe("yesterweb.m4a", beam_size=5, language="en", condition_on_previous_text=False, vad_filter=True)

print("Detected language '%s' with probability %f" % (info.language, info.language_probability))

for segment in segments:
    print("[%.2fs -> %.2fs] %s" % (segment.start, segment.end, segment.text))
```

I found `distill-large-v3` is better than `large-v3`. It takes roughly same amount of time to run as the audio. 

Results are with the timestamps you can easily get rid of them by changing last line.

```python
    print("%s" % (segment.text))
```

There is also a possibility of moving text directly in a text file.

```python
with open(f"mluther.txt", "w") as file:
        for segment in segments:
            file.write(f"{segment.text}\n")
```

I will use the following script in the future.

```python
from faster_whisper import WhisperModel
import os


filename = "mluther.mp3"
base_filename = os.path.splitext(os.path.basename(filename))[0]

model_size = "distil-large-v3"
model = WhisperModel(model_size, device="cpu", compute_type="int8")

segments, info = model.transcribe(filename, beam_size=5, language="en", condition_on_previous_text=False, vad_filter=True)
print("Detected language '%s' with probability %f" % (info.language, info.language_probability))

with open(f"{base_filename}.txt", "w") as file:
        for segment in segments:
            file.write(f"{segment.text}\n")
            
print("Done")
```

# Future

It would be beneficial to learn about another application that is based on faster-whisper but supports word-to-word editing. I came across [this one](https://github.com/geekodour/wscribe), which can generate a JSON file for transcripts, allowing for a word-to-word comparison between audio and transcript. This feature is helpful for correcting errors.

I believe this tool would be very useful for recording my voice notes. I will need to use a program to sift through the rambling. However, I think it's a great idea.