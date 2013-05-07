---
layout: project
title: Shipped
subtitle: "What did you do today?"
categories:
  - projects
links:
  - url: https://github.com/secondbit/shipped
    title: "Shipped on Github"
  - url: http://alpha.app.net/shipped
    title: "Paddy&apos;s Shipped account on App.net"
permalink: /shipped
repo: secondbit/shipped
unlisted: false
summary: "<p>Shipped is an App.net client with one purpose: to keep track of what you do every day.</p>"
---
Shipped is a very bare-bones, minimal client for [App.net](http://app.net). It does not let you read posts, it does not support attachments or images or anything else. It has one purpose, and one purpose only: it helps you keep track of what you do every day.

It&apos;s really easy to get caught up in being *busy* without actually being *productive*. Shipped was created to help us measure how much we were actually getting done each day, with the theory being that once we start to measure our productivity, our productivity will increase.

Paddy&apos;s eponoymous App.net account for this can be followed [here](http://alpha.app.net/shipped) if you&apos;re interested in keeping up with what he&apos;s doing every day.

To install Shipped, simply run `go get secondbit.org/shipped` (making sure your $GOPATH/bin folder is part of your PATH) and then run the `shipped` command. After setting up your access token the first time the program is run, you can write a brief message about what you did that will be posted to App.net. Every time you accomplish something during the day, take a couple seconds to ship it. You&apos;ll have a running log of everything you&apos;ve done.
