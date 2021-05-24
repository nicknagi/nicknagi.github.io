---
layout: default
title: Projects
---

# 2021
----------------------
## Physics Simulator
{% include technologies.html technologies="git rust" %}

<p></p>
<video controls loop>
  <source src="https://user-images.githubusercontent.com/14340000/117508795-27d1ab80-af57-11eb-9566-2863e8106ed3.mov">
Your browser does not support the video tag.
</video>

A newtonian physics simulator built in Rust. The main goal of the project was to learn the Rust programming language. 

Particles are modelled as circles in 2D space. Collision detection is used to simulate elastic collisions.

[Github Repository](https://github.com/nicknagi/rust-physics-simulation)


## Course Project: Distributed Key-Value Store
{% include technologies.html technologies="git java" %}

Project done as part of Winter 2021 ECE419 Distributed Systems course.

A distributed key-value store implemented from scratch in Java. The database uses consistent hashing to distribute keys among the nodes in the cluster. Replication is used to achieve fault-tolerance.