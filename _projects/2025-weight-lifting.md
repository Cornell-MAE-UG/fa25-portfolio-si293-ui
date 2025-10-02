---
layout: project
title: Weight Lifting Mechanism Overview
description: Just a spaceship that I designed
technologies: [Hand calculations]
image: /assets/images/weight-lifting.png
---


In ENGRD 2020, we were asked to come up with a design for the following prompt:

"Given a 2D design space of 150cm long and 50cm tall, a rigid bar of a fixed length (your choice), 3 pin supports of which two need to be mounted on the ground and a linear actuator (pick from <a href="https://www.tolomatic.com/wp-content/uploads/2022/05/2700-4000_29_IMA_cat.pdf">this</a> online catalog, use max force values only), design a frame/mechanism to lift the maximum possible weight to the highest possible height. Assume all the supports and bar/actuator are rigid."

<b>Solution:</b>

I chose to use the IMA linear actuator from the catalog. This was for two reasons. First is the fact that all of the linear actuators have a stroke length of at least 0.5m, which well exceeds the dimensions of available space. Therefore, I wanted to use the least overbuilt mechanism possible for my task. Also, the IMA was the only actuator with full performance and mechanical specifications available, so using it was good practice for fully understanding my mechanism. 

I defined my problem goal to be the heaviest mass that could be lifted to a height of 0.15 m. My general solution, simply based on the principle of torque, is shown below. 

<img src="weight-lifting-diagram.jpeg">