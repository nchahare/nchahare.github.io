---
title: "FFmpeg: changing aspect ratio"
layout: post
date: 2024-06-05
---

Twitter has specific requirements for video dimensions. It's essential to have a reasonable aspect ratio like 16:9 or 4:3, and the platform doesn't allow odd numbers of pixels in the width or height. It's also recommended to upload MP4 files for better compatibility.

**Step 1: Install FFmpeg on Windows**

1. Open your command prompt.
2. Type `winget install ffmpeg` and press enter.
3. Say yes to all prompts and restart the terminal when installation is complete.

**Method 1: Padding**

Padding involves adding black bars to the height of your video to meet Twitter's aspect ratio requirements. Here's how to do it:

1. Calculate the padding pixels. If your video's width (`iw`) is 680 and the height (`ih`) is 480 (4:3 aspect ratio), the `padding` would be `((680*3 - 480*4)/8)`.
2. Use the following FFmpeg command for padding:
    
    `ffmpeg -i input.mp4 -vf "pad=width=iw:height=ih+padding:x=0:y=padding/2:color=black" -c:a copy output.mp4`
    
    Replace `padding` with your calculated value.

**Method 2: Cropping**

Cropping is a simpler method where you remove parts of the video to meet the aspect ratio. Here's how:

1. Determine the crop width, crop height, x, and y values.
2. Use the following FFmpeg command for cropping:
    
    `ffmpeg -i input.mp4 -vf "crop=cw:ch:x:y" output.mp4`
    
    Replace `cw`, `ch`, `x`, and `y` with your values.

If you don't specify `x` and `y` then it will crop from the center.

**Convert avi to mp4**

If you need to convert avi to mp4 use following command

`ffmpeg -i input.avi output.mp4`

**References**

- You can learn many FFmpeg commands through this webapp https://ffmpeg.lav.io/
- Also, actual documentation: https://www.ffmpeg.org/ffmpeg.html
