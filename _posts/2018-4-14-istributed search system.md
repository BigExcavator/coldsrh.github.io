---
published: true
title: Distributed search system
category: Networking
tags: [Networking, Algorithm]
layout: post
---

##Introduction
This project is a simplified version of a lookup service(such as Google File System). 

In detail, a model of distributed lookup service where a single client issues a (dictionary) key search to a server which in turn searches for the key (and it's associated value) over 3 backend servers. The server facing the client then collects the results from the backend servers, performs additional computation on the results if required, and communicates it to the client in the required format.The monitor also receives the results from the server and will show the same result as the client side do.

The following picture shows the structure of the whole system:

![0](https://raw.githubusercontent.com/BigExcavator/coldsrh233.github.io/master/_posts/image/%23Distributed_System/0.jpg)

#Technologies
All the connections are based on TCP/UDP as shown by the picture

#Functions
The following picture shows the allowed operations:

![1](https://raw.githubusercontent.com/BigExcavator/coldsrh233.github.io/master/_posts/image/%23Distributed_System/1.jpg)

#The screen message of terminals
The following picture shows the screen message of aws server:

![2](https://raw.githubusercontent.com/BigExcavator/coldsrh233.github.io/master/_posts/image/%23Distributed_System/2.jpg)

The following picture shows the screen message of the backend server:

![3](https://raw.githubusercontent.com/BigExcavator/coldsrh233.github.io/master/_posts/image/%23Distributed_System/3.jpg)

The following picture shows the screen message of the client side:

![4](https://raw.githubusercontent.com/BigExcavator/coldsrh233.github.io/master/_posts/image/%23Distributed_System/4.jpg)

#what I learned 

I learned how to implement TCP/UDP connection using C++, and other details of socket programming. And it's a good experience for me
to get to know about how a simple distributed system worked. What's more, I implemented the searching for words using prefix/suffix in 
the real environment.



