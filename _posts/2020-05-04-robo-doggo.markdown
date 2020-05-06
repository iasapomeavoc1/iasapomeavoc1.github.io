---
layout: post
title: Robo-Doggo
date: 2020-05-04 00:00:00 +0300
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional) 
img: robo-doggo-primary.jpg # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Robotics, 3D-Printing, Raspberry Pi, Personal]
---

I've seen a great deal of progress in quadruped robotics over the years, from BigDog to SpotMini, and now widespread development at universities like the MIT Mini Cheetah or Stanford Doggo. I've always wanted to try my hand at developing a similiar but smaller, low cost robot for home enviornments. More specifically, I wanted to try and recreate the experience of a pet, with robotics. 

***

### Mechanical Design
I designed all custom parts in Solidworks, which incudes the leg mechanisms, brackets, and body platform. The legs are 3D printed in black PLA, and the body is a ABS plate that was cut and drilled by hand. 


<img align="right" width="300"  src="{{site.baseurl}}/assets/img/robo-doggo-primary.jpg">
<img align="right" width="300"  src="{{site.baseurl}}/assets/img/robo-doggo-1.jpg">
All four legs are identical, and are driven by three LX16-A servos. Two servos directly control the joint, while the third controls the last joint through a belt and pulley. 

The latest, printed design has split halves on each of the leg links, to allow for easy assembly of the belt and also an internal mechanism for ground contact sensing.

<br clear="all"/><br/>
<img align="right" width="300"  src="{{site.baseurl}}/assets/img/robo-doggo-4.jpg">
<img align="right" width="300"  src="{{site.baseurl}}/assets/img/robo-doggo-2.jpg">
<img align="right" width="300"  src="{{site.baseurl}}/assets/img/robo-doggo-3.jpg">

<br clear="all"/><br/>

***

### IK Control
<img align="center" height="400"  src="{{site.baseurl}}/assets/img/robo-doggo-1.gif">
<img align="center" height="400"  src="{{site.baseurl}}/assets/img/robo-doggo-2.gif">
<br clear="all"/><br/>

***

### Ball-Tracking Control
<img align="center" height="300"  src="{{site.baseurl}}/assets/img/robo-doggo-3.gif">
<br clear="all"/><br/>
<img align="center" height="400"  src="{{site.baseurl}}/assets/img/robo-doggo-4.gif">

<br clear="all"/><br/>
