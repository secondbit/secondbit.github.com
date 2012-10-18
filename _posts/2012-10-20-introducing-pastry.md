---
title: Introducing Pastry
author:
  name: Paddy Foran
  slug: paddy
categories:
  - posts
tags:
  - "author/paddy"
layout: post
---
We're really pleased to be open sourcing our first major project for [Go](http://www.golang.org): [Pastry](/pastry), an implementation of the [Pastry distributed hash table](http://en.wikipedia.org/wiki/Pastry_%28DHT%29) written entirely in Go.

<!-- break -->

## The Future Is Distributed

It's no secret that we love cloud computing here at Second Bit. We like the distributed nature of it. When software is built without single points of failure, it's easy to build software that scales well and has strong reliability built in from the start. We think this is a better way to build software.

As a distributed hash table, Pastry is going to help us in that endeavour. Distributed hash tables are most popular for their impact on peer-to-peer applications like BitTorrent, but they have a variety of uses. They help computers become self-organising, meaning the computers form a group that can tolerate computers coming and going without any breakdown in functionality. This is incredibly powerful, and it's a tool we're excited to be adding to our belt.

## Like A Really Badass Lego

Pastry isn't going to be used directly in any of our applications or services. Instead, it's going to be used as a building block: other tools and utilities will be built as [applications on top of Pastry](http://go.pkgdoc.org/secondbit.org/pastry#Application), taking advantage of its self-organising principles to do some pretty cool stuff. One of the projects we have in the pipeline, codenamed "Peter", is a realtime pub/sub network built on top of Pastry. It allows for fast, reliable message passing amongst any group of servers, incorporates new servers that enter the group, and doesn't break when a server is down. This is an extremely powerful tool, and the bulk of its power comes from Pastry's self-organising capabilities.

## Free As In Freedom

Pastry is licensed under the [MIT license](http://opensource.org/licenses/MIT), a permissive open source license that basically says you can do what you want as long as you don't sue us. We like not getting sued.

You can view the source [on Github](https://github.com/secondbit/pastry), and we have a very nice README that explains how to use the package and how to contribute. If you have any problems or want to report a bug, please just [open an issue](https://github.com/secondbit/pastry/issues/new), and we'll love you forever.
