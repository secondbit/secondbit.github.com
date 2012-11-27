---
title: Pastry Is Now Wendy
author:
  name: Paddy Foran
  slug: paddy
categories:
  - posts
tags:
  - "author/paddy"
layout: post
---
After we [introduced Pastry](/blog/introducing-pastry/) to the world and got a lot of feedback on it (as well as some awesome contributions from the Go community), we started thinking about the directions we'd like to take the project. We realised a lot of these directions strayed from the original Pastry paper in their approach to the problem, even if the goals were the same.

To avoid misleading developers that stumble across this package without being aware of the subtle distinctions, we're renaming the project to Wendy as of today.

<!-- break -->

## How to Upgrade

We're not currently aware of any projects that are actively using Pastry, which is the only reason we felt comfortable making this breaking change. We're still attempting to be cautious.

Code importing secondbit.org/pastry will automatically be served the new Wendy package, whose package name is "wendy" and has a few renamed variables and methods. This will probably break legacy code. All references to Pastry should be switched to Wendy, matching the case of the original, and that should be the only change needed to have code work again.

If you need the Pastry version of this package, we've tagged a "pastry" tag in Github that has the latest code available that uses the Pastry package name. Simply manually check that out and "go install" it, and you'll have the old version of the package available.

## Why Wendy?

We're big fans of Peter Pan here at Second Bit. It's kind of an unhealthy fixation we have. Because the distributed publish/subscribe network we're building is going to be named Peter, we thought it only appropriate that we name the distributed hash table that powered it Wendy.

## Comments? Concerns?

We've set up a [mailing list](http://groups.google.com/group/wendy-users) for people using Wendy to discuss the package on. While it may not get very much traffic, we'll use it to communicate future changes of this nature and get the feedback of people using the package, as well as to answer any questions. The point is simply to offer a way for the community to discuss the project, rather than hiding all these conversations across Hacker News, Reddit, and our private inboxes.
