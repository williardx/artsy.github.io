---
layout: post
title: 'Cocoa Architecture: Shared Process'
date: 2015-10-24T00:00:00.000Z
comments: false
categories:
  - ios
  - mobile
  - process
author: Orta Therox
github-url: 'https://www.github.com/orta'
twitter-url: 'http://twitter.com/orta'
blog-url: 'http://orta.io'
---

We've been asked a few times about [our](https://github.com/artsy/mobile/issues/64) [process](https://github.com/artsy/mobile/issues/47). As someone extremely interested in this, I've been running talks with other heads of mobile in NYC ( if you are one, [get in touch](https://twitter.com/orta/status/644298718636806144) ) to find out how other team's process their processes.

We have four developers, with four apps  on three separate product teams. So there's not too much overlap in how we work individually.  There is no definitive "this is the artsy mobile way." However, there are overlapping details in how we treat our apps.  I'm going to try look at where the overlaps in the app building process.

<!-- more -->

### Product Teams vs Practice

rough overview of the product teams vs practices, mention better documentation will be forthcoming
how team communicate
  - slack
  - trello
  - hangouts
remote working devs

### Agile

how much of the agile process do we actually do?
 - team standups tue/thur

### GitHub

- milestones
- issues
- labels
- cross-practice communication via labels/ pinging via product team members

### Multiple shared libs over `ArtsyKit`

- Simplifies dependency graph
- Easier to OSS libraries
- Easy to bootstrap a new apps
- major downsides though ATM

### Product

Interactions wth design via github issues
dropbox, slack
Meetups, question + design issues

### Test with the fastest, broadest brush possible.

shippers gonna ship, hard to know whether its worth testing if it's gonna get thrown away
snapshots as initial tests encapsulating change visually, then only unit tests covering "what changed"
no integration Tests
all code is PR'd

### Build your way, make sure others understand

MVVM / Reactive
alloy + vim, orta + appcode
expectation that you aren't just a cocoa dev, should know:
- command line
- ruby

### Avoid process that can take us away from building apps

Using travis/circle instead of Jenkins
Making CocoaPods plugins to hot-fix issues
  - https://github.com/ashfurrow/cocoapods-chillax-swift
  - https://github.com/orta/cocoapods-expert-difficulty
