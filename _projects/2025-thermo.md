---
layout: project
title: Thermodynamic Analysis of the Kohler Command Pro CH440 Used in Baja SAE Racing
description: Just a spaceship that I designed
technologies: [Hand calculations, Desmos]
image: /assets/images/bajarear.jpg
---
<p>In ENGRD 2210, we were asked to address the following prompt:</p>

<blockquote>
    <p>"Please select a real-world instance of a device or system that we have learned about in
    this course, explain how it works in detail, and then discuss how its performance would
    change under a change in design or operating conditions. Your report should include:</p>

    <ul>
        <li>Photos and schematics of the device or system</li>
        <li>A qualitative description of the device or system</li>
        <li>A system diagram of the device or system operating (either CV or CM), showing
            work and heat transfer interactions as well as any relevant mass flows</li>
        <li>Mass balance, energy balance, and entropy balance equations (as relevant)
            capturing the physics more central to the device or system operation</li>
        <li>Describe a change to device or system design or operating conditions and then
            how that change influences device performance"</li>
    </ul>
</blockquote>

Both I and my friend Arda Griffin are members of the Baja Racing team here at Cornell. We decided it would be interesting to analyze the Kohler Command Pro CH440 engine used in our car. All cars competing in the Baja SAE collegiate series are required to use this identical engine model, as it levels the playing field.

<img src="../../assets/images/ch440.jpeg" width=400px>

The CH440 produces 14 HP and is a single cylinder, four stroke engine––perfect for analyzing with the cold-air-standard Otto cycle. 

Using engine specs available online, we will first <b>calculate the engine's efficiency and mean effective pressure</b>, and then ____ and determine its effect on the engine's performance. First, some specs and assumptions.

<a href="https://www.engines.rehlko.com/products/CH440"><b>CH440 specifications:</b></a>
<ul>
    <li>Compression ratio: 8.0:1</li>
    <li>Engine displacement: 429 cc</li>
    <li>Peak power: 3600 rpm</li>
</ul>

<b>Assumptions</b>
<ul>
    <li>Using cold-air-standard model</li>
    <li>Assuming adiabatic and isochoric stages</li>
    <li>k = 1.4 (environment is room temperature and outside pressure is atmospheric</li>
</ul>

A real gasoline cycle can be modeled by the following 5 steps:

<img src="../../assets/images/tspv.jpg" width=400px>

Because combustion is a difficult process to model thermodynamically, we instead simplify the model to be a closed system with heat input and heat output, as follows:

<img src="../../assets/images/idealized4stroke.jpg" width=400px>

This much neater cycle, which assumes adiabatic and isochoric stages, has associated T-S and P-V diagrams, as shown below:

<img src="../../assets/images/real4stroke.jpg" width=400px>

to determine t3, using typical fuel energy of gasoline which 1500 kJ/kg air