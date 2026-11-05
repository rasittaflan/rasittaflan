<div align="center">

<img src="./assets/profile_banner.svg" alt="Muhammet Raşit Taflan — Engineering Portfolio Banner" width="100%" />

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-rasittaflan-0077b5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rasittaflan)
[![GitHub](https://img.shields.io/badge/GitHub-rasittaflan-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/rasittaflan)
[![Institution](https://img.shields.io/badge/KTÜ-Electrical_%26_Electronics_Engineering-0284c7?style=flat-square&logo=mortarboard&logoColor=white)](https://www.ktu.edu.tr/eee)

<br/>

**[English Portfolio](#about-me)** &nbsp;|&nbsp; **[Featured Projects](#featured-engineering-projects)** &nbsp;|&nbsp; **[Research & Experience](#research--engineering-experience)** &nbsp;|&nbsp; **[Türkçe Profil Özeti](#turkce-profil-ozeti)**

</div>

---

<a id="about-me"></a>

## 1. Professional Overview

I am a senior **Electrical & Electronics Engineering student** at **Karadeniz Technical University (KTU)**.

My engineering work focuses on solving physical engineering challenges through the integration of **numerical multiphysics modeling**, **power converter topologies**, and **closed-loop embedded control**. Rather than generic software development, my research and project activities center on:

* **Power Electronics & Conversion:** High-efficiency DC-DC topologies (Buck, Boost, LLC Resonant, Phase-Shifted Full-Bridge ZVS, Vienna PFC), magnetic design, and power semiconductor stress/thermal characterization.
* **Electromagnetic Simulation & FEA:** 2D/3D magnetostatic and transient finite element analysis using Ansys Maxwell and FEMM, focusing on flux density saturation ($B$-$H$ curves) and force-airgap-current dynamics.
* **Closed-Loop Control Dynamics:** Non-linear plant modeling, discrete-time feedback control, and PID + Anti-Windup algorithms in MATLAB/Simulink.
* **Embedded Hardware & Telemetry:** ARM Cortex-M (STM32) firmware development, hardware timer-triggered PWM, ADC sampling, and automotive CAN bus telemetry.

---

<a id="featured-engineering-projects"></a>

## 2. Featured Engineering Projects

All projects listed below are documented with full source code, simulation workbooks, and verifiable analytical results.

### Project 1: Electromagnetic Levitation (Maglev) FEA & System Dynamics Suite
> **TÜBİTAK 2209-B Industry-Oriented Undergraduate Research Project**  
> *Karadeniz Technical University — Department of Electrical & Electronics Engineering*

<div align="center">
  <img src="./assets/fea_magnetic_flux.png" alt="Ansys Maxwell 2D/3D Magnetic Flux Density Contour Plot" width="85%" />
  <p><em>Figure 1: Verified Ansys Maxwell magnetostatic flux density (B-Field) contour across core and 5.0 mm air gap.</em></p>
</div>

* **Problem Statement:** Contactless magnetic suspension systems for high-speed ground transportation (Hyperloop) and precision industrial motion are inherently open-loop unstable according to Earnshaw's Theorem. The physical lifting force exhibits severe non-linearity, varying inversely with the square of the air gap ($F \propto 1/g^2$).
* **Engineering Approach:** Developed an integrated workflow bridging finite element electromagnetic modeling in **Ansys Maxwell 2D Axisymmetric & 3D** with dynamic closed-loop control synthesis in **MATLAB/Simulink**.
* **Tools & Technologies:** `Ansys Maxwell 2D/3D`, `FEMM 4.2`, `MATLAB / Simulink`, `Three.js / WebGL`, `HTML5 / JavaScript`.
* **Technical Implementation:**
  * Modeled cylindrical and U-core electromagnets using Silicon Steel / Steel 1008 material models with non-linear saturation limits ($B_{sat} \approx 1.8\text{ T}$).
  * Executed adaptive mesh refinement until residual energy error converged below $0.1\%$.
  * Generated a discrete 3D lookup matrix ($F_{mag}$ vs. $g$ vs. $I$) and coupled it to a non-linear plant in Simulink with discrete-time PID + Anti-Windup control and thermal runaway bounds.
* **Verified Results:**
  * **V1 Cylindrical Actuator ($r = 5\text{ mm}, L = 30\text{ mm}$):** Verified lifting force of **$0.4823\text{ N}$** at $4.8\text{ A}$ excitation current across the nominal **$5.0\text{ mm}$ working air gap** ($22.26\text{ mN}$ at $1.0\text{ A}$).
  * **V2 Distributed Array Specification:** Research target defined at **$\ge 130\text{ N}$** for pod suspension integration.
  * Verified position stability under 300-second thermal endurance runs and external mechanical step disturbances.
* 📂 **Repository:** [`rasittaflan/Electromagnetic-Levitation-FEA-Simulations`](https://github.com/rasittaflan/Electromagnetic-Levitation-FEA-Simulations)
* 🚀 **Interactive Demo:** [Launch 3D WebGL Maglev Digital Twin](https://rasittaflan.github.io/Electromagnetic-Levitation-FEA-Simulations/) | [Live Calculation Studio](https://rasittaflan.github.io/Electromagnetic-Levitation-FEA-Simulations/Maglev_Canli_Hesaplayici.html)

---

### Project 2: Power Electronics — 16 SMPS Topologies Design & Live Formula Suite
> **Interactive Engineering Calculation Engine based on Texas Instruments Standards (SLYU036A & SLYW038B)**

* **Problem Statement:** Designing switch-mode DC-DC converters for industrial, automotive, and telecommunication systems requires evaluating multiple isolated and non-isolated topologies under strict semiconductor stress, duty cycle limits, and continuous/discontinuous conduction mode (CCM/DCM) boundaries.
* **Engineering Approach:** Developed a fully cross-verified engineering calculation suite that mathematically couples master spreadsheet engines (`.xlsx` & `.ods`) with zero-dependency browser-based analytical engines.
* **Tools & Technologies:** `Power Converter Modeling`, `TI SLYU036A & SLYW038B`, `JavaScript (ES6)`, `HTML5 / MathML`, `Microsoft Excel`, `LibreOffice Calc`, `LaTeX`.
* **Technical Implementation:**
  * Synthesized 16 fundamental SMPS DC-DC converters:
    * *Non-Isolated:* Buck, Boost, Inverting Buck-Boost, SEPIC, Ćuk, Zeta.
    * *Isolated:* Flyback, Two-Switch Flyback, Active Clamp Forward, Single-Switch Forward, Two-Switch Forward, Push-Pull, Weinberg, Half-Bridge, Full-Bridge, and Phase-Shifted Full-Bridge (PSFB - ZVS).
  * Formulated an analytical pipeline linking 14 user design input parameters to 25 continuous output variables per converter.
* **Verified Results:**
  * Formulated and numerically cross-verified **400 active engineering equations** with 100% numerical parity between Excel/Calc models and web engines.
  * Accurately calculates inductor current ripple ($\Delta I_L$), capacitor voltage ripple ($\Delta V_{out}$), semiconductor peak voltage/current stress, and Zero-Voltage Switching (ZVS) transition criteria.
* 📂 **Repository:** [`rasittaflan/Power_Electronics`](https://github.com/rasittaflan/Power_Electronics)
* 🚀 **Interactive Demo:** [Launch Live SMPS Calculator](https://raw.githack.com/rasittaflan/Power_Electronics/main/TI_16_Canli_Hesaplayici.html) | [Interactive LaTeX Reference Table](https://raw.githack.com/rasittaflan/Power_Electronics/main/TI_16_Guc_Kaynagi_Topolojisi_Interaktif_Tablo.html)

---

### Project 3: Bodrum Gulet Hybrid EMS — Renewable Power & Naval Stability Optimization
> **KTÜ MHN 4001 Interdisciplinary Engineering Capstone Project**  
> *Authors: Muhammet Raşit Taflan & Muhammed Emin Kadirov*

* **Problem Statement:** Traditional wooden Bodrum charter gulets (20–35 m) continuously run auxiliary diesel alternator sets 24 hours/day to sustain hotel electrical loads during bay anchorage, leading to fuel inefficiency, acoustic disturbance, soot, and marine emissions.
* **Engineering Approach:** Modeled and simulated a marine microgrid combining photovoltaic arrays, lithium energy storage, and auxiliary generation, governed by a rule-based discrete Energy Management System (EMS) while validating naval transverse intact stability.
* **Tools & Technologies:** `Discrete Energy Management FSM`, `Solar Position Astronomy`, `LiFePO4 Storage Modeling`, `Naval Hydrostatics`, `Three.js / WebGL`, `JavaScript`.
* **Technical Implementation:**
  * Implemented a discrete-time Finite State Machine (FSM) enforcing instantaneous Kirchhoff power balance across a 48 VDC distribution bus ($\Delta t = 5\text{ min}$, $|P_{balance}| < 10^{-9}\text{ kW}$).
  * Coupled an astronomical solar trajectory algorithm for Bodrum coordinates ($37.034^\circ\text{ N}, 27.430^\circ\text{ E}$) to compare **Model A (8.0 kWp Fixed Bimini Array)** against **Model B (13.6 kWp Retractable Solar Wings)** with 3500 N linear actuator thrust and wind-speed safety interlocks.
* **Verified Results:**
  * **71.6% diesel fuel reduction:** Daily consumption decreased from $88.42\text{ L/day}$ (baseline) to $25.10\text{ L/day}$ (Model B).
  * **17.6 hours daily silent operation:** Generator runtime reduced from 24.0 h/day down to 6.4 h/day.
  * **20.36 tons seasonal $\mathrm{CO}_2$ avoided** over a standard 120-day charter season.
  * **Naval stability validated:** Transverse metacentric height ($GM = 1.021\text{ m}$, $\Delta KG = +9.4\text{ mm}$), confirming form stability compliance.
* 📂 **Repository:** [`rasittaflan/Bodrum-Gulet-Hybrid-EMS-Simulator`](https://github.com/rasittaflan/Bodrum-Gulet-Hybrid-EMS-Simulator)
* 🚀 **Interactive Demo:** [Launch 3D WebGL Marine EMS Simulator](https://rasittaflan.github.io/Bodrum-Gulet-Hybrid-EMS-Simulator/)

---

<a id="research--engineering-experience"></a>

## 3. Research & Engineering Experience

### ⚡ Vestel R&D — Hardware Design Engineering Intern
**Electric Vehicle Charging Systems** • *Summer 2026 (6-Week Intensive Hardware R&D)*  
* Investigated power converter topologies for next-generation EV charging stations, focusing on high-efficiency isolated DC-DC stages including **LLC Resonant Converters** and Zero-Voltage Switching (ZVS) **Phase-Shifted Full-Bridge (PSFB)**.
* Evaluated three-phase **Vienna PFC** rectifiers and **interleaved boost** input stages for harmonic reduction and power factor correction.
* Participated in semiconductor loss calculations, capacitor ripple current budgeting, thermal stress validation, and CAN bus telemetry verification in high-power test laboratory environments.

---

### 🧲 TÜBİTAK 2209-B — Undergraduate Research Project
**Electromagnetic Levitation & Hyperloop Systems** • *2024 – Present*  
* *Project Title:* "Design of PID Controlled Electromagnetic Levitation System and Its Integration into Hyperloop Applications".
* Conducted 2D/3D magnetostatic finite element analysis, air-gap flux mapping, and coil thermal dissipation modeling.
* Synthesized closed-loop feedback algorithms coupling Maxwell FEA data with Simulink dynamic plant models.

---

### 🏎️ Ege University Electric Vehicle Team — Former Team Captain
**Electric Race Vehicle Engineering** • *August 2023 – September 2024*  
* Led the multidisciplinary engineering team through design, integration, wiring harness assembly, and track testing of an energy-efficient electric competition vehicle.
* Oversaw Battery Management System (BMS) cell monitoring, high-voltage safety interlocks, motor controller parameter tuning, and CAN bus telemetry acquisition.
* Ensured full compliance with technical race regulations and electrical safety standards.

---

### 🚝 Hyperloop Engineering Team
**Levitation, Propulsion & Dynamics Subsystems** • *2024 – Present*  
* Contributed to subsystem hardware engineering across electromagnetic levitation coils, linear induction propulsion concepts, power distribution, and dynamic stability.

---

<a id="technical-competencies"></a>

## 4. Technical Competencies

The competencies listed below reflect tools, methods, and technologies applied directly in research projects, laboratory work, and engineering coursework:

| Competency Domain | Core Tools & Frameworks | Practical Engineering Application |
| :--- | :--- | :--- |
| **Power Electronics** | DC-DC Converters, LLC Resonant, PSFB (ZVS), Vienna PFC, Buck/Boost Topologies | High-efficiency converter design, magnetic core/inductor design, semiconductor stress and thermal loss analysis. |
| **Control & Simulation** | MATLAB, Simulink, Simscape, State-Space, Classical Control | Non-linear dynamic plant modeling, discrete-time PID + Anti-Windup control, closed-loop stability verification. |
| **Electromagnetics & FEA** | Ansys Maxwell (2D/3D), FEMM 4.2 | Magnetostatic & transient field analysis, B-H saturation analysis, coil inductance calculation, air-gap force mapping. |
| **Embedded Systems** | C, C++, ARM Cortex-M (STM32), STM32CubeIDE | Bare-metal & HAL firmware, timer-triggered PWM, ADC sampling, interrupt service routines, CAN, UART, SPI, I2C. |
| **Engineering Software** | Python (NumPy / SciPy), JavaScript, HTML5 / MathML, LaTeX, Git, GitHub | Discrete numerical modeling, interactive calculation engines, version control, technical documentation. |
| **Laboratory Instrumentation** | Digital Storage Oscilloscopes, Power Analyzers, Electronic Loads, LCR Meters | Power stage waveform debugging, current ripple measurement, thermal endurance testing, bench validation. |

---

<a id="education--certifications"></a>

## 5. Education & Academic Background

* **Bachelor of Science in Electrical & Electronics Engineering**  
  **Karadeniz Technical University (KTU)**, Trabzon, Türkiye  
  *Expected Graduation: 2026*  
  *Relevant Coursework:* Power Electronics, Control Systems, Electromagnetic Field Theory, Microprocessors, Electrical Machines, Signals & Systems.

---

<a id="github-activity"></a>

## 6. GitHub Activity

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=rasittaflan&show_icons=true&theme=tokyonight&hide_border=false&bg_color=0b1329&title_color=38bdf8&text_color=94a3b8&icon_color=00f2fe&border_color=1e293b" alt="Rasit Taflan GitHub Stats" height="155" />
&nbsp;
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=rasittaflan&layout=compact&theme=tokyonight&hide_border=false&bg_color=0b1329&title_color=38bdf8&text_color=94a3b8&border_color=1e293b" alt="Top Languages" height="155" />

</div>

---

<a id="turkce-profil-ozeti"></a>

## 7. 🇹🇷 Türkçe Profil Özeti

> [!NOTE]
> Tam kapsamlı, bağımsız Türkçe portföy dokümanı için [**👉 README_TR.md**](README_TR.md) dosyasını inceleyebilirsiniz.

### Genel Tanıtım & Mühendislik Yaklaşımı
**Muhammet Raşit Taflan**, Karadeniz Teknik Üniversitesi (KTÜ) Elektrik-Elektronik Mühendisliği 4. sınıf lisans öğrencisidir.

Çalışmaları, salt yazılım geliştiriciliğinden ziyade **güç elektroniği**, **sonlu elemanlar analizi (FEA)**, **gömülü sistemler** ve **kapalı çevrim kontrol dinamikleri** alanlarında gerçek fiziksel mühendislik problemlerine yönelik tasarım, analiz, simülasyon ve Ar-Ge faaliyetlerine odaklanmaktadır.

### Başlıca Uzmanlık Alanları
* **Güç Elektroniği & Güç Dönüşümü:** 16 temel SMPS DC-DC dönüştürücü topolojisi (Buck, Boost, Flyback, Forward, Köprü topolojileri), yüksek verimli Faz Kaydırmalı Tam Köprü (**PSFB - ZVS**), **LLC Rezonans** dönüştürücüler, üç fazlı **Vienna PFC** doğrultucular ve manyetik bileşen tasarımı.
* **Sonlu Elemanlar Analizi (FEA) & Manyetik Simülasyon:** Ansys Maxwell 2D/3D ve FEMM ortamlarında manyetik akı yoğunluğu, B-H eğrisi manyetik doyumu ($B_{sat} \approx 1.8\text{ T}$), hava aralığı ve aktüatör kuvveti analizi.
* **Gömülü Sistemler & Kontrol:** STM32 (ARM Cortex-M) mimarisi üzerinde C/C++ gömülü yazılım, donanımsal PWM üretimi, ADC örnekleme, kapalı çevrim **PID + Anti-Windup** denetleyiciler ve CAN bus haberleşmesi.
* **Yenilenebilir Hibrit Enerji Sistemleri:** Güneş PV, LiFePO4 batarya ve yardımcı dizel jeneratör tabanlı sistemlerin sonlu durum makinesi (FSM) tabanlı akıllı enerji yönetimi (EMS).

### Öne Çıkan Deneyimler
1. **Vestel Ar-Ge — Donanım Tasarımı Stajı (2026):** Elektrikli araç şarj sistemlerinin güç dönüştürücü donanım tasarımı, LLC rezonans ve PSFB topolojileri, termal stres testleri ve laboratuvar ölçümleri.
2. **TÜBİTAK 2209-B Araştırma Projesi:** *"PID Kontrollü Elektromanyetik Levitasyon Sistemi Tasarımı ve Hyperloop Uygulamalarına Entegrasyonu"*. Ansys Maxwell FEA modellemesi ile 5 mm hava aralığında $0.4823\text{ N}$ @ $4.8\text{ A}$ V1 kuvvet doğrulaması ve Simulink kontrol tasarımı.
3. **Ege Üniversitesi Elektrikli Araç Takımı — Eski Takım Kaptanı (2023–2024):** Elektrikli yarış aracının batarya yönetim sistemi, telemetri, düşük gerilim mimarisi ve teknik yarış regülasyonları yönetimi.
4. **Disiplinlerarası Mühendislik Tasarımı (KTÜ MHN 4001):** *"Bodrum Guletlerinde Yenilenebilir Hibrit Güç ve Akıllı EMS Optimizasyonu"*. %71.6 yakıt tasarrufu, 17.6 saat sessiz seyir modu ve enine stabilite doğrulaması.

---

<a id="contact--linkedin"></a>

## 8. Contact & Professional Links

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
