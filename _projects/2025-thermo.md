---
layout: project
title: Thermodynamic Analysis of the Kohler Command Pro CH440 Used in Baja SAE Racing
description: Just a spaceship that I designed
technologies: [Hand calculations]
image: /assets/images/bajarear.jpg
---

<!-- MathJax for LaTeX equation rendering -->
<script>
MathJax = {
  tex: {
    inlineMath: [['$', '$'], ['\\(', '\\)']],
    displayMath: [['$$', '$$'], ['\\[', '\\]']]
  }
};
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

<style>
body {
    font-family: Georgia, serif;
    max-width: 900px;
    margin: auto;
    line-height: 1.6;
    padding: 20px;
}
h1, h2, h3 {
    font-family: "Times New Roman", serif;
}
code {
    background: #f0f0f0;
    padding: 3px 5px;
}
</style>

<body>

<p>In ENGRD 2210, we were asked to address the following prompt:</p>

<blockquote>
    <p><em>"Please select a real-world instance of a device or system that we have learned about in
    this course, explain how it works in detail, and then discuss how its performance would
    change under a change in design or operating conditions. Your report should include:</em></p>

    <ul>
        <li><em>Photos and schematics of the device or system</em></li>
        <li><em>A qualitative description of the device or system</em></li>
        <li><em>A system diagram of the device or system operating (either CV or CM), showing
            work and heat transfer interactions as well as any relevant mass flows</em></li>
        <li><em>Mass balance, energy balance, and entropy balance equations (as relevant)
            capturing the physics more central to the device or system operation</em></li>
        <li><em>Describe a change to device or system design or operating conditions and then
            how that change influences device performance"</em></li>
    </ul>
</blockquote>

<h2>Background</h2>

<p>My friend Arda Griffin and I are members of the Baja Racing team here at Cornell. We decided it would be 
interesting to analyze the Kohler Command Pro CH440 engine used in our car. All cars competing in the Baja SAE 
collegiate series are required to use this identical engine model, as it levels the playing field.</p>

<img src="../../assets/images/ch440.jpeg" width=400px>

<p>The CH440 produces 14 HP and is a single cylinder, four-stroke engine—perfect for analyzing with the 
cold-air-standard Otto cycle. Arda and I will do the following:</p>
<b><ol>
    <li>Calculate the Otto effiency and MEP of the CH440 assuming room temperature operating conditions</li>
    <li>Recalculate these values assuming 0&deg; operating conditions, simulating the effect of enhancing the engine with a cold air intake</li>
    <li>Compare the two efficiencies to show why standardized engine hardware is necessary to ensure fairness in SAE competitions</li>
</ol></b>

<h2>Engine Specifications and Assumptions</h2>

<p><strong>CH440 Specifications:</strong></p>
<ul>
    <li>Compression ratio: 8.0:1</li>
    <li>Engine displacement: 429 cc</li>
    <li>Peak power: 3600 rpm</li>
    <li>Produces 14HP in real life</li>
</ul>

<p><strong>Analysis Assumptions:</strong></p>
<ul>
    <li>Using cold-air-standard model</li>
    <li>Assuming adiabatic and isochoric stages</li>
    <li>$\gamma = 1.4$ (environment is room temperature and outside pressure is atmospheric)</li>
</ul>

<h2>Real vs. Idealized Cycles</h2>

<p>A real gasoline cycle can be modeled by the following 5 steps:</p>

<img src="../../assets/images/real2.jpg" width=400px>

<p>Because combustion is a difficult process to model thermodynamically, we instead simplify the model 
to be a closed system with heat input and heat output, as follows:</p>

<img src="../../assets/images/ideal2.jpg" width=400px>

<p>This much neater cycle, which assumes adiabatic and isochoric stages, has associated T-S and P-V diagrams, 
as shown below:</p>

<img src="../../assets/images/tspv2.jpg" width=400px>

<h2>Performance Calculations</h2>

<p>This analysis evaluates the ideal Otto cycle performance of a 429 cc,
single-cylinder, four-stroke spark-ignition engine operating with an
air-standard model. The following values are our inputs (all based on our previous assumptions––see above):</p>

<p>
\[
T_1 = 300\ \text{K}, \quad r = 8, \quad \gamma = 1.4,
\]
\[
P_1 = 100\ \text{kPa}, \quad R = 287\ \text{J/kg K}, \quad V_d = 4.29\times10^{-4}\ \text{m}^3.
\]
</p>

<p>We also need need to define how much heat gets added in to our cycle during the fake "combustion" process. To do this, we define:
<p>
\[
q_{in} = 1.5\times 10^{6}\ \text{J/kg}
\]

<p> where \( q_{in} \) is roughly the specific heat capacity of ignited gasoline. The specific heat at constant volume is evaluated using the ideal gas relation:</p>

<p>
\[
c_v = \frac{R}{\gamma - 1}
     = \frac{287}{0.4}
     = 717.5\ \text{J/kg K}.
\]
</p>

<h4>1. Compression Process (1 → 2)</h4>

<p><strong>Assumption:</strong> The compression stroke is adiabatic and reversible (isentropic).  
This neglects friction and heat loss to the cylinder walls, giving an upper bound on real engine performance.</p>

<p>
\[
T_2 = T_1 r^{\gamma-1}
    = 300 \cdot 8^{0.4}
    = 689\ \text{K}.
\]
\[
P_2 = P_1 r^{\gamma}
    = 100 \cdot 8^{1.4}
    = 1.84\ \text{MPa}.
\]
</p>

<p>The cylinder volumes follow:</p>

<p>
\[
V_1 = \frac{r}{r-1}V_d = \frac{8}{7}(4.29\times10^{-4})
    = 4.90\times 10^{-4}\ \text{m}^3,
\]
\[
V_2 = \frac{V_1}{r}
    = 6.13\times10^{-5}\ \text{m}^3.
\]
</p>

<h4>2. Heat Addition (2 → 3)</h4>

<p><strong>Assumption:</strong> Combustion is modeled as instantaneous heat addition at constant volume.  
This allows all added energy to raise temperature and pressure without piston motion.</p>

<p>
\[
T_3 = T_2 + \frac{q_{in}}{c_v}
    = 689 + \frac{1.5\times10^6}{717.5}
    = 2781\ \text{K}.
\]
\[
P_3 = P_2 \frac{T_3}{T_2}
    = 1.84\times 10^{6}
      \left(\frac{2781}{689}\right)
    = 7.42\ \text{MPa}.
\]
</p>

<h4>3. Expansion (3 → 4)</h4>

<p><strong>Assumption:</strong> The expansion is isentropic, meaning all thermal energy is converted to useful work with no heat loss.  
This provides the theoretical maximum power output.</p>

<p>
\[
T_4 = T_3 r^{1-\gamma}
    = 2781 \cdot 8^{-0.4}
    = 1210\ \text{K},
\]
\[
P_4 = P_3 r^{-\gamma}
    = 7.42\times10^{6} \cdot 8^{-1.4}
    = 0.403\ \text{MPa}.
\]
\[
q_{out} = c_v(T_4 - T_1)
        = 717.5(1210 - 300)
        = 6.53\times10^{5}\ \text{J/kg}.
\]
</p>

<h4>4. Cycle Efficiency and Work</h4>

<p><strong>Assumption:</strong> Only thermodynamic losses inside the ideal cycle are considered.  
Mechanical friction, pumping losses, and real combustion inefficiencies are excluded.</p>

<p>
\[
w_{net} = q_{in} - q_{out}
        = 8.47\times10^{5}\ \text{J/kg}.
\]
\[
\eta = \frac{w_{net}}{q_{in}}
     = 0.564
     = 56.4\%.
\]
</p>

<h4>5. Mass per Cycle and Work Output</h4>

<p><strong>Assumption:</strong> The mass of air inside the cylinder is computed from the ideal gas law at state 1, assuming perfect volumetric efficiency.</p>

<p>
\[
m = \frac{P_1 V_1}{RT_1}
  = 5.68\times10^{-4}\ \text{kg}.
\]
\[
W_{\text{cycle}} = m\, w_{net}
                 = 482\ \text{J}.
\]
\[
\text{MEP} = \frac{W_{\text{cycle}}}{V_d}
            = 1.12\ \text{MPa}.
\]
\[
P_{ind} = 482 \cdot 30
        = 14.46\ \text{kW}
        \approx 19.40\ \text{HP}.
\]
</p>

<p>Comparing to the real life CH440 power output of 14 HP:</p>

<p>
\[
\mu_{\text{real}} = \frac{14}{19.40} \approx 72.6\%.
\]
</p>

<h4>Summary of Results (Room Temp.)</h4>

<p>
\[
\eta_{} = 56.4\%, \quad
\text{MEP} = 1.12\ \text{MPa}, \quad
\mu_{\text{real}} \approx 72.6\%.
\]
</p>

<script>
MathJax = {
  tex: {
    inlineMath: [['$', '$'], ['\\(', '\\)']],
    displayMath: [['$$', '$$'], ['\\[', '\\]']]
  }
};
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

<style>
body {
    font-family: Georgia, serif;
    max-width: 900px;
    margin: auto;
    line-height: 1.6;
    padding: 20px;
}
h1, h2, h3 {
    font-family: "Times New Roman", serif;
}
code {
    background: #f0f0f0;
    padding: 3px 5px;
}
</style>

<body>

<br><br><br>
<hr><hr>
<br><br><br>

<h2>Performance Calculations (0°C Intake Temperature)</h2>

<p>
This second analysis repeats the first analysis done but assumes near-freezing intake temperature, which accurately simulates driving conditions in the dead of winter here in Ithaca. For simplicity, we'll assume a "cold" temperature correspodns to 0°C. In regular cars, cold air intakes are an aftermarket upgrade to fuel economy, so we expect to see a slight increase in efficiency. Calculation assumptions for each process remain the same as before.
</p>

<p>The new cold-air intake temperature is:</p>

<p>
\[
T_1 = 273\ \text{K} \quad (0^\circ\text{C})
\]
</p>

<p>
Cold air is denser and has a slightly higher ratio of specific heats. We use:
</p>

<p>
\[
\gamma = 1.403, \qquad R = 287\ \text{J/(kg\,K)}
\]
</p>

<p><strong>Assumed constants (unchanged from the warm-air case):</strong></p>
<ul>
    <li>Heat input: \( q_{in} = 1.5\times10^{6}\ \text{J/kg} \)</li>
    <li>Displacement: \( V_d = 4.29\times10^{-4}\ \text{m}^3 \)</li>
    <li>Compression ratio: \( r = 8 \)</li>
</ul>

<p>
The specific heat at constant volume for near-freezing intake air is:
</p>

<p>
\[
c_v = \frac{R}{\gamma - 1}
     = \frac{287}{0.403}
     = 712.9\ \text{J/(kg\,K)}.
\]
</p>

<h4>1. Compression Process (1 → 2)</h4>

<p>
\[
T_2 = T_1 r^{\gamma-1}
    = 273 \cdot 8^{0.403}
    = 629\ \text{K},
\]
\[
P_2 = P_1 r^{\gamma}
    = 100\cdot 8^{1.403}
    = 1.877\ \text{MPa}.
\]
</p>

<p>Cylinder volumes:</p>

<p>
\[
V_1 = \frac{r}{r-1}V_d = 4.90\times10^{-4}\ \text{m}^3,
\]
\[
V_2 = \frac{V_1}{r} = 6.13\times10^{-5}\ \text{m}^3.
\]
</p>

<h4>2. Heat Addition (2 → 3)</h4>

<p>
\[
T_3 = T_2 + \frac{q_{in}}{c_v}
    = 629 + 2103
    = 2732\ \text{K},
\]
\[
P_3 = P_2 \frac{T_3}{T_2}
    = 8.15\ \text{MPa}.
\]
</p>

<h4>3. Expansion Process (3 → 4)</h4>


<p>
\[
T_4 = T_3 r^{1-\gamma}
    = 2732 \cdot 0.434
    = 1185\ \text{K},
\]
\[
P_4 = P_3 r^{-\gamma}
    = 0.434\ \text{MPa}.
\]
\[
q_{out} = c_v(T_4 - T_1)
        = 6.51\times10^{5}\ \text{J/kg}.
\]
</p>

<h4>4. Cycle Efficiency and Work</h4>


<p>
\[
w_{net} = q_{in} - q_{out}
        = 8.49\times10^{5}\ \text{J/kg},
\]
\[
\eta = \frac{w_{net}}{q_{in}}
     = 0.566
     = 56.6\%.
\]
</p>

<h4>5. Mass per Cycle and Work Output</h4>


<p>
\[
m = \frac{P_1 V_1}{R T_1}
  = 6.23\times10^{-4}\ \text{kg},
\]
\[
W_{\text{cycle}} = m\, w_{net}
                 = 529\ \text{J},
\]
\[
\text{MEP} = \frac{W_{\text{cycle}}}{V_d}
            = 1.23\ \text{MPa},
\]
\[
P_{ind} = 529 \cdot 30
        = 15.87\ \text{kW}
        \approx 21.28\ \text{HP}.
\]
</p>

<p>Comparing to the CH440’s real output at 0°C (≈16.3 HP):</p>

<p>
\[
\mu_{\text{real}} = \frac{16.3}{21.28} \approx 76.6\%.
\]
</p>

<h2>Summary of Results (0&deg;)</h2>

<p>
\[
\eta = 56.6\%, \quad
\text{MEP} = 1.23\ \text{MPa}, \quad
\mu_{\text{real}} \approx 76.6\%.
\]
</p>

<h2>Comparisons / Conclusions</h2>

<p>
The cold air analysis shows that, as expected, cold intake air boosts Otto efficiency by a small amount (0.2%)! It's neat to see that a process that can be understood from a general car performance perspective but then also backed up with calculations. Taken together, these calculations demonstrate the need for SAE to ban all engine modifications––with a cold air intake, some cars would be able to go longer without refueling during our Endurance race (an unfair advantage).
</p>