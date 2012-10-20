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
We're really pleased to be open sourcing something we've been working on for a long time now: [Pastry](/pastry), an implementation of the [Pastry distributed hash table](http://en.wikipedia.org/wiki/Pastry_%28DHT%29) written entirely in [Go](http://www.golang.org). We're only comfortable calling it an "alpha release" right now, so you may not want to run any mission-critical software on it just yet, but it's ready to be kicked around a bit.

<!-- break -->

## Six Months In The Making

In April, we ran across a problem while we were developing the next iteration of [2cloud](/2cloud). We had already written an API, and we had already written a WebSockets server, and while they were living on the same machine, everything was fine. But when we wanted to split them up so we could scale horizontally, we ran into a problem.

How would the WebSockets server know about events that occurred in the API?

We could have just written a quick TCP connection between the two and called it a day. But when we needed to add another WebSockets server so we could handle more requests, we'd have to edit the API code. Ew.

We could have just written a quick server that sits in the middle and fans events sent to it by the API servers out to all the WebSockets servers, but that would have created a single point of failure and a bottleneck for the system. No thanks.

We could have just used Redis' pub/sub features to distribute the events, but again, that's another bottleneck and another single point of failure. One that happens to be our database, as well. That just seems like asking for trouble.

We couldn't seem to find any way to subscribe to events and publish events without a single point of failure. We looked at everything we could find, and they all seemed to have this bottleneck.

So we set out to build our own.

## A Really Badass Lego

Pastry, on its own, doesn't solve this problem for us. Pastry is really good at one thing: making servers self-organising. As a distributed hash table, Pastry helps your application quickly and efficiently route messages amongst any number of servers. The problem is, it's not multi-cast; a message will only get delivered to a single Node. What happens if we have multiple WebSocket servers, or the message gets delivered to an API server? That's no good.

But it does take care of that whole "sending messages" thing.

The cool thing is, Pastry isn't just a package on its own; it can be built on. We supply [an interface](http://go.pkgdoc.org/secondbit.org/pastry#Application) that you can fill in your own applications to receive callbacks from Pastry when significant events in the cluster happen.

Our next project is a package (codenamed Peter) that will handle the publishing and subscribing aspects, which will finally solve our problem.

## Open Source

We love open source, so Pastry is licensed under the permissive [MIT License](http://opensource.org/licenses/MIT). Use it, abuse it, do what you will with it. Just please don't sue us.

If you'd like to contribute, we love you. There's [information in the README](https://github.com/secondbit/pastry#contributing) about how to do that. It's pretty straight-forward: fork us, modify the source, go fmt it (like a good little Gopher), and send us a pull request. Not so bad, right?

If you notice something wrong with Pastry, run into a bug, or have a suggestion, we'd love it if you'd [open an issue](https://github.com/secondbit/pastry/issues/new). We like pull requests more, but issues are awesome, too.

## Get Go-ing

We had to make at least one Go pun.

You can get Pastry in a way that should be familiar to any Go user by now: run "go get secondbit.org/pastry" on your commandline. Yes, we used a vanity URL. Sue us.

You can find the [source](https://github.com/secondbit/pastry) on Github. You'll see some [instructions](https://github.com/secondbit/pastry/#use) on how to use it in the README.

We're really excited to be releasing Pastry today, even in this alpha form. Feel free to [let us know what you think](/contact). We'd love to hear from you.

![Distribute ALL the things!](/images/posts/distribute-all-the-things.jpg)
