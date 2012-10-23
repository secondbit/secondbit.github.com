---
layout: project
title: Pastry
subtitle: "Pastry: A distributed hash table written in Go"
categories:
  - projects
permalink: /pastry
repo: secondbit/pastry
links:
  - url: "https://github.com/secondbit/pastry"
    title: "Pastry on Github"
  - url: "http://go.pkgdoc.org/secondbit.org/pastry"
    title: "Documentation"
summary: "<p>Pastry is an implementation of the Pastry distributed hash table algorithm. Written in Go, it provides a basic building block for distributed applications.</p>"
---
Pastry is an implementation of the [Pastry distributed hash table](http://www.wikipedia.org/wiki/Pastry_%28DHT%29). Written in [Go](http://www.golang.org), it provides a basic building block for distributed applications.

<!-- break -->

Please [see our discussion about the future of pastry](https://github.com/secondbit/pastry/issues/7).

## Purpose

Pastry does one thing, and it does it very well: it lets a cluster of servers become self-organising. That means servers can send messages between each other with no central hub, no single point of failure. Servers, referred to as Nodes, can simply announce their presence and begin passing messages with the rest of the group.

Using Pastry is simple. You create a Node and build a Cluster around it. If this is the first Node to join, that's it, you're done! If there's already a Node in the Cluster, you simply announce your presence to it. That Node will take care of telling the other Nodes, and they'll all tell you about the other Nodes in the Cluster. Then you can just start passing messages. When a Node leaves, you'll just reroute the message to a new Node, and the Cluster will move on. For code examples on how to accomplish all of this, check the [README](https://github.com/secondbit/pastry/#use) or the [documentation](http://go.pkgdoc.org/secondbit.org/pastry).

## License

Pastry is licensed under the [MIT license](http://opensource.org/licenses/MIT). You can find its source code on [Github](https://github.com/secondbit/pastry), which is incidentally where you can also [report issues](https://github.com/secondbit/pastry/issues/new) or, if you're feeling generous, [send pull requests](https://github.com/secondbit/pastry/pull/new/master).
