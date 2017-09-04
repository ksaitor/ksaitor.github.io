---
layout: post
title: "Parameterized Jenkins build for rollback purposes."
description: ""
date: 2014-04-22
tags: ['guide']
comments: true
---


Yes, I know, Jenkins is terrible. I don’t recommend using it. Use TravisCI, CircleCI or something like that.

Nonetheless. If u happen to use Jenkins for whatever reason, there are advantages to it. One of them is manually trigger-able and parameterized builds. With them, you can set up rollbacks to a specified git tag.
When emergency hits (hope it’s not) you’ll need this.

- Tick “This build is parameterized”:
![1](/images/parameterized-jenkins-build-for-rollback-purposes/1.png)

- In “Source Code Management” specify your git repo and click “Advanced…”
![2](/images/parameterized-jenkins-build-for-rollback-purposes/2.png)

- And there enter the following magic: `+refs/tags/$GIT_TAG:refs/remotes/origin/tags/$GIT_TAG`
![3](/images/parameterized-jenkins-build-for-rollback-purposes/3.png)
How I came up with this — trial+error+stackoverflow

- Branches to build: `*/tags/$GIT_TAG`
![4](/images/parameterized-jenkins-build-for-rollback-purposes/4.png)
After this, you’ll want to configure the rest of the build in your preferred fashion… whatever takes to actually build and deploy your repo… Click ‘Save’ and you are done.

Settings mentioned above are key to ensure successful checkout of a git tag you’ll specify in the following step.

- Click “Build with Parameters” in the top left menu. Enter git tag as a parameter. Click “Build” and profit!
![4](/images/parameterized-jenkins-build-for-rollback-purposes/4.png)

Let me know how did this work for you!
You should follow me up at @ksaitor and subscribe to this blog below.

Btw, [this post originally appeared on my other blog.](http://blog.ramanshalupau.com/parameterized-jenkins-build-for-rollback-purposes) 
