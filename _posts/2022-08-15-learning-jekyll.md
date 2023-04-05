---
title: "Making a webpage using Jekyll"
author: Nimesh Chahare
date: 2022-08-15
tags: notes
layout: post

---

One of the best things I found on the internet. Basically I was browsing my twitter feed and some random person said "you need to have a personal website. Use this webinar to make it with jekyll." At this point of time I already had this webpage with my CV. But I realized that I can't really have nice things like navigation bar or side bar or any other bar in my website.

I even had hard time putting the images in. This was all because my reluctance to install jekyll and rubygems on my computer. I was using github site directly in my browser. So I took a look at this [video](https://youtu.be/7SBXl94xNl8). It finally looked easy and doable. So I decided to give it another shot.


I used the following commands:

First download ruby+devkit from [here](https://jekyllrb.com/docs/installation/windows/). Follow the instructions.

```cmd
ruby -v

gem install bundler
gem install jekyll


jekyll -v
```

Then make a directory and open "Mingw64" github stuff.

```cmd
jekyll new myblog
cd myblog

bundle install
bundle exec jekyll serve
```

Last two commands will be used all the time.

I was able to edit and make pages all along by following these links:

GitHub repo: [https://github.com/laurburke2/laurbur...](https://github.com/laurburke2/laurburke2.github.io))



Finally following are the commands for the git.

```git
git remote add origin
https://<PERSONAL_ACCESS_TOKEN>@github.com/<username>/<username>.github.io.git

git add .
git commit -m "Initial Commit"
git remote -v
git push origin master
```



My final webpage looks like [this](nchahare.github.io)
