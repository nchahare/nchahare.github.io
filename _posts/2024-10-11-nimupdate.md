---
title: "Combining sudo apt update+upgrade"
author: Nimesh Chahare
layout: post
date: 2023-12-14
tags: resources
---

I am not a frequent Ubuntu user, but I use it enough to find it frustrating to repeatedly type `sudo apt update`, enter my password, and then type `sudo apt upgrade`. I thought I was the only one who felt this way, but it turns out many others share this annoyance, and there is a simple solution to address it.

We can create an alias for a set of commands in the `.bashrc` file, and the computer will remember it.

## How I created `nimupdate`

This is the alias we will use:

```
# Custom alias for updating system
nimupdate() {
    echo "Starting system update..."
    sudo apt update && sudo apt upgrade -y
    echo "System update completed."
}
```

Next, add this to the `.bashrc` file.

Follow these steps:
- Open the terminal.
- Type `nano ~/.bashrc`.
- Scroll down to the end and paste the command by right-clicking.
- To save, press `Ctrl + X`.
- Exit the nano editor.
- Type `source ~/.bashrc`.
- Restart the terminal for the command to take effect.
- Try using `nimupdate`. It will prompt for your password, and then it should work.