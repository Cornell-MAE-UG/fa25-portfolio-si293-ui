---
layout: project
title: Open Design Project
description: Just a spaceship that I designed
technologies: [LaTeX]
image: /assets/images/slf.jpg
---

<div style="clear: left;"></div>

[Client Pitch](#client-pitch) | [Functional Prototype](#functional-prototype) | [Client Report](#client-report)
<br>
<br>
The Open Design Project was the biggest project we completed for MAE 2250: Intro to Mechanical Design. It was centered around the premise of designing (but mostly just pitching) a mechanical solution to spotted lanternfly infestation of vineyards. Spotted lanternflies are a huge problem for vineyards in NYS and currently the only solution to their infestation is to monitor them extremely vigilantly and use a variety of pesticides and netting whenever possible as prevention. You might think that the purpose of an Intro to Mechanical Design class would be to learn and practice mechanical design, but this project really just turned into a bunch of rather pointless design without any possibility whatsoever of empirical testing. But at least we got a lot of practice pitching useless ideas to uninterested audiences (just like the real world)! Anyways, below are some of the deliverables my group created for the project.

## Client Pitch

<img src="../../assets/images/ODP_Client1.jpg" style="width:100%;" />

<img src="../../assets/images/ODP_Client2.jpg" style="width:100%;" />

## Functional Prototype

#### Purpose

The purpose of our prototype was to test the main rotational mechanism of our strainer. We wanted to determine whether it could turn without too much resistance, hold water, and support weight. In accomplish this, we didn't need to fabricate the entire body of our strainer. Instead, we just fabricated the bottom part, along with the base, crankshaft, and handle. We then conducted a series of three tests to answer our queries. 

#### Tests and Results

**Rotation test**

The rotation test was meant to assess the ability of the handle, shaft, and base components to rotate freely beneath the divider of the cylinder. It was performed by rotating the shaft using the handle and observing the smoothness and ease of motion of the base. Success criteria for this test was that the base would be able to be rotated using a non-strenuous amount of force from a human hand at the handle, and that the mesh would not noticeably interfere with the dividers upon rotation. 

The results of this test were informative. First, we observed smooth rotation of the base when low to moderate force was applied to the handle, indicating effective tolerancing on the interface between the base and cylinder to limit friction. Second, however, we noticed that the edges of the mesh, particularly the epoxy connections, momentarily jammed rotation when they passed under the dividers. 

For the next iteration, to resolve this, we plan to create an indentation in the base for the mesh to rest within, allowing the top of the mesh to sit at the same height as the rest of the base and pass under the divider without impeding rotation. 

**Water retention test**

The water retention test was meant to check the seal and water retention of the cylinder and base. It was performed by filling the cylinder with water for 15 minutes and observing leaks in the points of connection in the cylinder (Figure 12).

The results of this test were also informative. The test showed us that the prototype was very poorly sealed, such that the volume of water drained out within two minutes. However, we noticed that some points of connection were better sealed than others. The diameter of the base was tightly connected with the cylinder; most of the leaking came through the connection points between the dividers and the base. 

We plan to resolve this issue by better developing a seal system between the dividers and the base. Specifically, we will purchase rubber flaps from McMaster to attach to the bottoms of the dividers, sealing the gap and reducing leakage.  

<img src="../../assets/images/water_retention_testing.png" style="width:200px;" />

*Figure 12: Water retention testing*

**Weight test**

The weight test was performed to test the strength of our base, cylinder, and rotation system in functioning under increased loads. It was performed by adding weights to the base in ~550g increments (Figure 13) and 1) observing any physical deformation in our design, and 2) rotating the handle and making note of ease of rotation. 

The test provided valuable insight as to how our design functions under increased loads. First, we noticed that as weight was added, the gap between the base and the dividers marginally increased, lowering friction and making rotation occur more smoothly (but also implying increased water leakage). Second, we noticed that if our design is used in such a way where only one out of three sections is filled with mixture at a given time, this unevenly distributed weight will cause the base to tilt down at an angle, greatly inhibiting water retention and structural integrity. Last, we noticed that the numeric limit to functionality of rotation of our cylinder fell at approximately 2.0 kg – any weight beyond this caused greatly angled deflection of the base. 

These results have important design implications. The first observation, regarding the widening gap between the dividers and the base, indicated that a support system beneath the base is quite necessary — the shaft collar and press fit between the shaft and base is not sufficient to vertically support the load. This was not a surprise or concern, as our design already accounts for placing bolts under the base — we were just not able to incorporate them into this prototype due to tolerancing issues (see Assembly section). The second observation will ideally also be resolved by this solution, as the vertical support provided by the bolts will prevent the observed angled deflection. However, we also plan to explore optimizing our design so that two out of three sections can be filled and filtered simultaneously — which would not only increase efficiency, but help limit the observed angled deflection due to more even distribution of loading.

<img src="../../assets/images/weight_testing.png" style="width:200px;" />

*Figure 13: Weights used for weight testing*

## Client Report