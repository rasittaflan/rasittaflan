<div align="center">

<img src="./assets/profile_banner.svg" alt="Muhammet Raşit Taflan — Engineering Portfolio Banner" width="100%" />

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-rasittaflan-0077b5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rasittaflan)
[![GitHub](https://img.shields.io/badge/GitHub-rasittaflan-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/rasittaflan)
[![Institution](https://img.shields.io/badge/KTÜ-Electrical_%26_Electronics_Engineering-0284c7?style=flat-square&logo=mortarboard&logoColor=white)](https://www.ktu.edu.tr/eee)

<br/>

**[About](#1-personal-introduction)** &nbsp;|&nbsp; **[Featured Projects](#2-featured-engineering-projects)** &nbsp;|&nbsp; **[Research & Experience](#3-research--engineering-experience)** &nbsp;|&nbsp; **[Technical Skills](#4-technical-competencies)** &nbsp;|&nbsp; **[Education](#5-education--academic-background)** &nbsp;|&nbsp; **[Contact](#6-contact--professional-links)** &nbsp;|&nbsp; **[🇹🇷 Türkçe Profil (README_TR.md)](README_TR.md)**

</div>

---

<a id="1-personal-introduction"></a>

## 1. Personal Introduction

I am a 4th-year **Electrical & Electronics Engineering student** at **Karadeniz Technical University (KTU)** (*Expected Graduation: 2027*).

My engineering studies center on the intersection of **power electronics**, **electromagnetic multiphysics modeling**, and **embedded closed-loop control systems**. My technical background spans:

* **Power Electronics & Conversion:** Switch-mode DC-DC converter topologies, magnetics sizing, inductor/capacitor ripple analysis, and semiconductor operating stress calculation.
* **Electromagnetics & Numerical Simulation:** 2D magnetostatic finite element analysis (FEA) using Ansys Maxwell and FEMM, focusing on air-gap magnetic flux density, B-H core saturation, and force generation.
* **Control Systems & Plant Dynamics:** Non-linear plant modeling, discrete-time feedback control, and PID + Anti-Windup algorithms in MATLAB/Simulink.
* **Embedded Hardware & Firmware:** Bare-metal C development on ARM Cortex-M microcontrollers (**Nuvoton M032KG** and **STM32**), hardware timer PWM generation, multi-channel ADC sampling, and UART/CAN telemetry.

> [!NOTE]
> **Academic & Open-Source Integrity:** All open-source projects hosted on this profile are independent personal and academic research efforts. They are developed without proprietary corporate tools, internal design files, or commercial IP, and are completely separated from corporate employment.

---

<a id="2-featured-engineering-projects"></a>

## 2. Featured Engineering Projects

All featured projects below include verifiable calculation engines, reproducible simulation models, and accessible documentation.

---

### Project 1: Electromagnetic Levitation FEA & Closed-Loop Control
> **TÜBİTAK 2209-B Industry-Oriented Undergraduate Research Project**  
> *Karadeniz Technical University — Department of Electrical & Electronics Engineering*

* **Engineering Problem:** Contactless electromagnetic suspension (EMS) for high-speed ground transit (Hyperloop) and industrial positioning is inherently open-loop unstable according to Earnshaw's Theorem. Lifting force is non-linear and inversely proportional to the square of the air gap ($F \propto 1/g^2$), requiring coupled electromagnetic field and dynamic control synthesis.
* **Technical Approach:** Combined numerical finite element analysis (FEA) in **Ansys Maxwell 2D Axisymmetric** with closed-loop dynamic feedback control in **MATLAB/Simulink**.
* **Implementation:**
  * Modeled a cylindrical electromagnet with a Steel 1008 core ($r = 5\text{ mm}, L = 30\text{ mm}$) and a 500-turn copper coil ($d = 0.7\text{ mm}$).
  * Configured adaptive mesh refinement with a 1.0% target error criterion in Ansys Maxwell Magnetostatic solver.
  * Formulated non-linear plant equations in MATLAB/Simulink; designed a discrete-time PID + Anti-Windup position regulator with simulated current and thermal saturation limits.
* **Results & Verification:**
  * *FEA Numerical Output (V1 Actuator):* Ansys Maxwell 2D magnetostatic analysis calculated a static lifting force of **$F_z = 22.26\text{ mN}$ at $1.0\text{ A}$** and **$F_z \approx 0.482\text{ N}$ at $4.8\text{ A}$** across a **$5.0\text{ mm}$ air gap**.
  * *Dynamic Simulation Status:* Closed-loop stabilization and step-disturbance rejection verified across 300-second non-linear Simulink simulations.
  * *Design Target:* Multi-actuator distributed pod suspension target set at $\ge 130\text{ N}$ for V2 development.
* 📂 **Repository:** [`rasittaflan/Electromagnetic-Levitation-FEA-Simulations`](https://github.com/rasittaflan/Electromagnetic-Levitation-FEA-Simulations)
* 🚀 **Interactive Demo:** [3D WebGL Digital Twin](https://rasittaflan.github.io/Electromagnetic-Levitation-FEA-Simulations/) | [Live Force Calculator](https://rasittaflan.github.io/Electromagnetic-Levitation-FEA-Simulations/Maglev_Canli_Hesaplayici.html)

---

### Project 2: Power Electronics Design Suite — 16 SMPS Topologies
> **Independent Open-Source Engineering Calculation & Educational Engine**  
> *Formulated from Texas Instruments Standard Literature (SLYU036A & SLYW038B)*

* **Engineering Problem:** Systematic design and comparative evaluation of switch-mode DC-DC converters across varying voltage ratios requires evaluating continuous/discontinuous conduction modes (CCM/DCM), duty cycle boundaries, semiconductor peak stress, and component sizing across 16 isolated and non-isolated topologies.
* **Technical Approach:** Developed an independent analytical calculation suite cross-verifying mathematical spreadsheet workbooks (`.xlsx` & `.ods`) with an interactive, zero-dependency browser-based analytical engine.
* **Implementation:**
  * Covers 16 topologies: Buck, Boost, Inverting Buck-Boost, SEPIC, Ćuk, Zeta, Flyback, Two-Switch Flyback, Active Clamp Forward, Single-Switch Forward, Two-Switch Forward, Push-Pull, Weinberg, Half-Bridge, Full-Bridge, and Phase-Shifted Full-Bridge (PSFB - ZVS).
  * Formulated an analytical pipeline linking 14 user design inputs to 25 continuous output variables per converter topology.
* **Results & Verification:**
  * *Analytical Consistency:* Implemented **400 active engineering equations** with 1:1 numerical parity between spreadsheet workbooks and the web engine.
  * *Physics-Based Derivations:* Formulates inductor current ripple ($\Delta I_L$), output voltage ripple ($\Delta V_{out}$), semiconductor peak reverse voltage/current stress, and Zero-Voltage Switching (ZVS) transition criteria.
  * *Independence:* Strictly an independent educational and research project; contains no corporate IP, proprietary test data, or commercial circuitry.
* 📂 **Repository:** [`rasittaflan/Power_Electronics`](https://github.com/rasittaflan/Power_Electronics)
* 🚀 **Interactive Demo:** [Live SMPS Calculator](https://raw.githack.com/rasittaflan/Power_Electronics/main/TI_16_Canli_Hesaplayici.html) | [Interactive Formula Reference Table](https://raw.githack.com/rasittaflan/Power_Electronics/main/TI_16_Guc_Kaynagi_Topolojisi_Interaktif_Tablo.html)

---

### Project 3: Bodrum Gulet Hybrid EMS Simulator
> **KTÜ MHN 4001 Interdisciplinary Engineering Capstone Project**  
> *Co-Authors: Muhammet Raşit Taflan & Muhammed Emin Kadirov*

* **Engineering Problem:** Traditional wooden charter gulets (20–35 m) continuously run auxiliary diesel alternator sets 24 hours/day while anchored to sustain hotel electrical loads, resulting in excess fuel consumption, acoustic emissions, and localized environmental impact.
* **Technical Approach:** Modeled and simulated a marine microgrid combining photovoltaic generation, LiFePO4 battery energy storage, and auxiliary diesel generation, governed by a rule-based discrete Energy Management System (EMS) while evaluating naval transverse intact stability.
* **Implementation:**
  * Built a discrete-time Finite State Machine (FSM) enforcing strict Kirchhoff power balance across a 48 VDC bus ($\Delta t = 5\text{ min}$, balance residual $|P_{\mathrm{balance}}| < 10^{-9}\text{ kW}$).
  * Integrated astronomical solar trajectory modeling for Bodrum coordinates ($37.034^\circ\text{ N}, 27.430^\circ\text{ E}$) to evaluate **Model A (8.0 kWp Fixed Bimini)** vs. **Model B (13.6 kWp Retractable Solar Wings)** under wind-speed aerodynamic safety limits.
* **Results & Verification:**
  * *Simulation Estimate:* Daily diesel fuel consumption reduced by **71.6%** (from $88.42\text{ L/day}$ baseline to $25.10\text{ L/day}$ in Model B).
  * *Operational Estimate:* Auxiliary generator runtime reduced from 24.0 h to 6.4 h, enabling **17.6 hours of continuous silent operation** daily.
  * *Environmental Projection:* Estimated **20.36 tons of seasonal $\mathrm{CO}_2$ avoided** over a 120-day charter season.
  * *Preliminary Hydrostatics:* Calculated transverse metacentric height ($GM = 1.021\text{ m}$, $\Delta KG = +9.4\text{ mm}$), confirming compliance with basic intact form stability criteria.
* 📂 **Repository:** [`rasittaflan/Bodrum-Gulet-Hybrid-EMS-Simulator`](https://github.com/rasittaflan/Bodrum-Gulet-Hybrid-EMS-Simulator)
* 🚀 **Interactive Demo:** [3D WebGL Marine EMS Simulator](https://rasittaflan.github.io/Bodrum-Gulet-Hybrid-EMS-Simulator/)

---

### Project 4: Signals & Systems Interactive Engineering Simulation & Active Learning Laboratory
> **KTÜ ELK3015 Signals and Systems — Analytical Simulation Engine & 8-Stage Digital Tutorial Platform**  
> *Author & Developer: Muhammet Raşit Taflan — Karadeniz Technical University (KTU)*

* **Engineering & Educational Objective:** Bridging the gap between abstract time/frequency-domain mathematical operators (convolution integrals/sums, Fourier series convergence, Laplace $s$-plane pole-zero geometry) and physical engineering intuition requires coupling real-time numerical simulation with structured active-learning pedagogy.
* **Technical & Pedagogical Approach:** Engineered a zero-dependency client-side computational laboratory and interactive self-paced tutorial system ("öğretici mühendislik dershanesi") covering the 14-week KTÜ ELK3015 curriculum across 4 core modules and 11 analytical topics.
* **Implementation:**
  * **6 Real-Time Mathematical Simulators (`Chart.js` + Custom Stem Canvas + `KaTeX`):** Continuous-time axis transformation synthesizer $y(t)=x(at-b)$, even/odd signal decomposition $x_e(t)+x_o(t)$, discrete moving-average filter $y[n]=\frac{1}{M}\sum_{k=0}^{M-1}x[n-k]$, step-by-step discrete convolution engine $y[n]=\sum x[k]h[n-k]$ (*Flip, Shift, Multiply, Accumulate*), Fourier Series Gibbs phenomenon harmonic synthesizer ($N \in [1, 49]$), and Laplace $s$-plane Region of Convergence (ROC) & BIBO stability analyzer.
  * **8-Stage Active Learning Tutorial Flow:** Every topic guides the student through *1. Physical Intuition $\rightarrow$ 2. Rigorous Mathematical Formulation $\rightarrow$ 3. Geometric Visual Interpretation $\rightarrow$ 4. Worked Analytical Example $\rightarrow$ 5. Live Parameter Sandbox $\rightarrow$ 6. Concept Check $\rightarrow$ 7. Exam Trap Alert $\rightarrow$ 8. Self-Assessment Mini-Quiz*.
  * **3-Mode Past Exam Solution Center:** Features 8 comprehensive midterm/final problems with progressive scaffolding (*Hint Mode* $\rightarrow$ *Step-by-Step Derivation* $\rightarrow$ *Full Exam-Sheet Proof*) and a 100% offline-capable local distribution.
* **Results & Verification:**
  * *Numerical & Structural Verification:* **10/10 automated Python unit tests** (`test_math_models.py` & `test_data_integrity.py`) verifying odd/even reconstruction error $< 10^{-15}$, discrete convolution sum parity, Gibbs overshoot (~9%), and $s$-plane BIBO stability rules ($	ext{Re}\{p_k\} < 0$).
* 📂 **Repository:** [`rasittaflan/Signals-and-Systems-Interactive-Lab`](https://github.com/rasittaflan/Signals-and-Systems-Interactive-Lab)
* 🚀 **Interactive Demo:** [Live Signals & Systems Interactive Lab](https://rasittaflan.github.io/Signals-and-Systems-Interactive-Lab/)

---

<a id="3-research--engineering-experience"></a>

## 3. Research & Engineering Experience

### 🏢 Vestel R&D | Hardware Design Intern — Summer 2026
Completed a six-week internship in hardware R&D related to electric vehicle charging systems. Gained experience with general power electronics concepts, converter topologies, engineering verification practices, and collaborative R&D workflows.

---

### 🧲 TÜBİTAK 2209-B — Undergraduate Research Project
**Electromagnetic Levitation & Control** • *Karadeniz Technical University (KTU)*  
* *Project Title:* "Design of PID Controlled Electromagnetic Levitation System and Its Integration into Hyperloop Applications".
* Conducted 2D magnetostatic finite element analysis, air-gap flux density calculations, and coil thermal dissipation modeling.
* Synthesized discrete-time closed-loop feedback algorithms coupling Maxwell FEA data with Simulink dynamic plant models.

---

### 🏎️ Ege University Electric Vehicle Team — Former Team Captain
**Electric Competition Vehicle Engineering** • *August 2023 – September 2024*  
* Led the multidisciplinary student engineering team through design, component integration, low-voltage wiring harness assembly, and track testing for an energy-efficient electric competition vehicle.
* Supervised Battery Management System (BMS) cell monitoring, high-voltage safety interlocks, motor controller parameter tuning, and CAN telemetry.
* Ensured technical compliance with competition electrical safety regulations.

---

### 🚝 Hyperloop Team Engineering
**Levitation & Dynamics Subsystems**  
* Contributed to student engineering studies on electromagnetic levitation actuators, linear induction propulsion concepts, power distribution, and dynamic stability.

---

<a id="4-technical-competencies"></a>

## 4. Technical Competencies

The competencies listed below reflect tools, methods, and hardware applied directly in academic research, student team engineering, laboratory testing, and engineering coursework:

| Competency Domain | Core Tools & Frameworks | Practical Engineering Application |
| :--- | :--- | :--- |
| **Power Electronics** | DC-DC Converters, LLC Resonant, PSFB (ZVS), Vienna PFC, Buck/Boost Topologies | Converter analytical design, magnetic core/inductor calculations, semiconductor stress and thermal loss analysis. |
| **Control & Simulation** | MATLAB, Simulink, Simscape, State-Space, Classical Control | Non-linear dynamic plant modeling, discrete-time PID + Anti-Windup control, closed-loop stability verification. |
| **Electromagnetics & FEA** | Ansys Maxwell 2D, FEMM 4.2 | 2D magnetostatic field analysis, B-H core saturation modeling, coil inductance calculation, air-gap force mapping. |
| **Embedded Systems** | **Nuvoton M032KG** (ARM Cortex-M0), **STM32** (ARM Cortex-M), C, GCC, VS Code, Nu-Link, STM32CubeIDE | Bare-metal firmware development, hardware timer PWM generation, multi-channel ADC acquisition, UART communication, CAN bus. |
| **Engineering Software** | Python (NumPy / SciPy), JavaScript, HTML5 / MathML, LaTeX, Git, GitHub | Discrete numerical modeling, interactive calculation engines, version control, technical documentation. |
| **Laboratory Instrumentation** | Digital Storage Oscilloscopes, Power Analyzers, Electronic Loads, LCR Meters | Power stage waveform debugging, current ripple measurement, thermal verification, bench validation. |

---

<a id="5-education--academic-background"></a>

## 5. Education & Academic Background

* **Bachelor of Science in Electrical & Electronics Engineering**  
  **Karadeniz Technical University (KTU)**, Trabzon, Türkiye  
  *Status:* 4th-Year Undergraduate Student &nbsp;|&nbsp; *Expected Graduation:* **2027**  
  *Relevant Coursework:* Power Electronics, Control Systems, Electromagnetic Field Theory, Microprocessors, Electrical Machines, Signals & Systems.

---

<a id="6-contact--professional-links"></a>

## 6. Contact & Professional Links

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect_on_LinkedIn-0077b5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rasittaflan)
[![GitHub](https://img.shields.io/badge/GitHub-Follow_on_GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/rasittaflan)

<br/>

```
Muhammet Raşit Taflan
Department of Electrical & Electronics Engineering
Karadeniz Technical University (KTU) | Trabzon, Türkiye
LinkedIn: https://www.linkedin.com/in/rasittaflan
GitHub:   https://github.com/rasittaflan
```

---

*Disciplined engineering analysis, physical simulation, and research-driven hardware design ⚡*

</div>

---

<div align="center">

**[🇹🇷 Bu profilin Türkçe versiyonu için tıklayınız (README_TR.md)](README_TR.md)**

</div>
