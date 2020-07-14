---
layout: post
title: Bike-Computer
date: 2020-07-13 00:00:00 +0300
description: Custom designed 3D printed bike computer
img: bc-4.jpg # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [3D-Printing, Raspberry Pi, Electronics Packaging, Personal]
---

During the 2020 pandemic, I bought a bike. As I became a full fledged bike enthusiast, I started looking at all the add-ons I could fit up my ride with. It shocked me how expensive bike computers were, while being a fairly dumb piece of electronics. Since I had some extra Pi's laying around, and wanting to dust off the 3D printer, I started designing up my own, with a couple extra features you won't see off the shelf.

My system includes a Raspberry Pi, 3.5" touchscreen LCD display, a GPS module, integrated camera, an Arduino Mini, and a Li-ion battery with power regulator. There is a sealed 12 pin connector to relay signals to and from other features on the bike, including an IMU, rear blinker lights, and hall-effect sensors to measure speed and cadence. The total cost comes at around $130, which was totally worth the fun designing and building this.

Note, this build is still in progress, so you won't see completed pictures just yet.

***

### Mechanical Design

After defining the scope and features of the system, I shopped around for electronics parts that would be necessary to integrate. The first step was then to start laying all the components out in CAD, to see what would be a good packaging arrangement. 

<img align="right" width="250"  src="{{site.baseurl}}/assets/img/bc-2.jpg">

<img align="right" width="250"  src="{{site.baseurl}}/assets/img/bc-1.jpg">

I wanted to keep the package thin and low to the bike handlebar, and opted to package some components on either side of the middle bar that I would be clamping the system to.
Once the sub components were roughly in position, I used a master modeling method within the assembly to create the structures necessary to mount and enclose them all. Happy with how it fit, I started my first print. 
<br/><br/>

<img style="display: block;max-width: 100%;height: auto;margin: auto;float: none!important;" width="500"  src="{{site.baseurl}}/assets/img/bc-7.jpg">

Engineering is an iterative process, and luckily the methods I was using to design and build are considered "rapid" prototyping. In this first build, I was immediately struck with how large the system looked on the bike, and potentially how much drag it would induce in my riding. I started immediately on a second packaging design after laying out this print. 

<br/><br/>

<img align="left" width="300"  src="{{site.baseurl}}/assets/img/bc-11.jpg">
<img align="left" width="300"  src="{{site.baseurl}}/assets/img/bc-4.jpg">
<img align="left" width="300"  src="{{site.baseurl}}/assets/img/bc-3.jpg">
<br/><br/>
<img align = "left" width="300"  src="{{site.baseurl}}/assets/img/bc-5.jpg"> Exploded View. 
<br/><br/>
<img align = "right" width="300"  src="{{site.baseurl}}/assets/img/bc-6.jpg"> The lower enclosure is the most complex part, having the most interfaces to other components, and requires about 11 hours to print with the settings I'm using. 
<br/><br/>
<img style="display: block;max-width: 100%;height: auto;margin: auto;float: none!important;" width="800"  src="{{site.baseurl}}/assets/img/bc-8.jpg"> <center>Most subcomponents of the system laid out.</center>
<br/><br/>
<img align="right" width="300"  src="{{site.baseurl}}/assets/img/bc-9.jpg"> The enclosure sealing surface is at an angle to the screen sealing surface. I prioritize the larger enclosure sealing surface to be flat, which resulted in the other surfaces to come out a bit jagged due to the resolution of the printer. I might try sanding down a bit, otherwise I could just use a gap filling silicone adhesive to seal the uneven surfaces.
<br/><br/>
<img align="left" width="300"  src="{{site.baseurl}}/assets/img/bc-12.jpg"> To clamp the computer to the bike, I designed a snap fit pincer type mount that would hook into depressions in the base of the enclosure. This is yet to be physically tested, but hopefully it provides a sturdy connection while also being easy to remove the computer from the hold by hand.

I designed all custom parts in Solidworks, which incudes the enclosures, bike clamps, internal mounting brackets, and the layout of electrical components on the internal PCB. The parts were printed in blue ABS, and will be sanded, painted and seal coated later. The electrical components are hand soldered to a through hole breadboard PCB. 

<br/><br/>

***

### Electrical Design

A 2200 mAh battery was used for this system. Summing the current consumption of the Pi, Arduino, camera and LCD screen, this gives over 2 hours of continuous use before recharge. With the brake lights on, this could be reduced to 1 hour. 

I'm using standard USB connectors to deliver power and send data. I cut open off the shelf USB cables to reduce the packaging size of the protruding connector and get the right cable length for all the intenral connections. The Arduino will send info to the Raspberry Pi via a serial connection.

An internal harness will be built up to route the wall mounted connector pins to the various pins on the Arduino. 

***


### Software Design

An interface for a bike info display showing speed, cadence, angle, acceleration and elevation will need to be developed. I also want to integrate a GPS navigation system to be able to map routes around the 7x7 area of San Francisco. All recordable biking stats and info can be logged to a server when the pi is on a Wifi network, and a site to showcase the stats can be built. Other software functionality can be rolled in later as well.



