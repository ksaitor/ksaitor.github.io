---
layout: post
title: 'fatal: CRLF would be replaced by LF'
description: ''
date: 2017-11-14
tags: ['git', 'engineering', 'howto']
og-image: 'https://media.giphy.com/media/AbDb2PniluFwY/giphy.gif'
---

![Pusheen Coding](https://media.giphy.com/media/AbDb2PniluFwY/giphy.gif) This is my favorite issue! 😻 Why? Because each
time this happens, i rush to Google and my [gist.github.com](https://gist.github.com/ksaitor) to find where I saved my
magic conversion code snippet.

- Run this twice: `git config --global core.autocrlf false`
- Do git add again

However, if you'd like to convert just one file or files one by one, then you can run this line:

```
perl -pi -e 's/\r\n/\n/g' input.file
```

Good luck coding! 🦄
