---
title: "Euler vs Quaternion - What's the difference?"
date: 2023-11-03T19:53:33+05:30
draft: false
author: "Gaudham P"
tags:
  - Unity 3D
  - Game Programming
  - 3D Math
# image: /images/post.jpg
description: ""
toc: false
---

| Eulers     | Quaternions |
|------------|------------|
| Easier for human understanding |   The 4th dimension makes it quite harder to visualize|
|Susceptible to Gimbal lock| Obviously safer and will not Gimbal lock|
|Order of operation does matter heavily|Order of operations does not matter|
|Two different values can mean the same thing|Each is unique and unambiguous|
|0 to 360 works as is, easier to make a backflip action|Takes the shortest route, e.g. a backflip will require two segmented operation of 0-180.|

Explained cleaner in the Youtube video below.

<br>
{{< youtube sJcVJEOwLUs >}}
<br>