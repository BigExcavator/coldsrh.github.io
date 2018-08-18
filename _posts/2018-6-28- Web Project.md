---
published: true
title: Online learning website (lighter version of Coursera)
category: Web Project
tags: 
  - Java Spring
layout: post
---

# Introduction

The website contains all of the basic functions an online learning website should have, and could be depolyed by Tomcat in localhost, or in public using SAE platform. The project include three terminals: the user-PC side, the manager-PC side, the user-Wechat side, and  all the three sides are separated.

# Functions

On the user end, the users can: Looking up all the courses on the courseList page, seeing the details about a course in the courseDetail page, learning the course on the courseLearing page, commenting on the courses in the comment area. What's more, the users can change their personal information.

On the operator&manager side, the managers can: manage the courses, teachers, course's sections, course's comments. In addition, they can obtain statistical charts and post recommended courses.

On the Wechat end, students can see their person infomation and their current courses.

The following picture shows the home page of the website.

![0](https://raw.githubusercontent.com/BigExcavator/coldsrh233.github.io/master/_posts/image/%23java_spring/0.jpg)

The following picture shows the courseLearning page.

![1](https://raw.githubusercontent.com/BigExcavator/coldsrh233.github.io/master/_posts/image/%23java_spring/1.jpg)

The following picture shows the statistical charts page.

![2](https://raw.githubusercontent.com/BigExcavator/coldsrh233.github.io/master/_posts/image/%23java_spring/2.jpg)

# Structure of the project

The project include two jar packages: ocCommon.jar, ocService.jar. THe ocCommon package include some basic functions like page division, user Authentication. The ocService package include all the operations that related to database.

The project also include three war packages: ocPortal, ocOperator, ocWechat. The ocPortal is the user-PC side, the ocOperator is the manager-PC side, the ocWechat is the user-Wechat side. The three war packages are built on the two jar packages.

The following picture shows the package structure of the project.

![3](https://raw.githubusercontent.com/BigExcavator/coldsrh233.github.io/master/_posts/image/%23java_spring/3.jpg)


# What I learned from the project

Maven: I learned how to use maven to manage Web project. Including using maven to manage all the related packages, using the pom.xml to import all the direct or indirect dependencies. 

Front End: Even though my main focus is on back end, I still get to know about how to use freemarker, how to write simple js code, and how to read and locate the code I want from the front pages.

Back End: I got familiar with the Spring MVC development process, and all the details related to it. What's more, I practiced my writting of sql.

Deployment: I learned how to publish my website on the SAE platform, it's a almost free and convenient platform for our learners to use.

<<<<<<< HEAD

=======
>>>>>>> 44ee501518cc71f3dcd25d9a14e0bed324646aee






