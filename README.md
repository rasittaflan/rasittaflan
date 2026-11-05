<div align="center">

<img src="./assets/profile_banner.svg" alt="Muhammet Raşit Taflan — Electrical & Electronics Engineer" width="100%" />

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Muhammet_Raşit_Taflan-0077b5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rasittaflan)
[![GitHub](https://img.shields.io/badge/GitHub-rasittaflan-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/rasittaflan)
[![Institution](https://img.shields.io/badge/Institution-Karadeniz_Technical_University-0284c7?style=for-the-badge&logo=mortarboard&logoColor=white)](https://www.ktu.edu.tr/eee)
[![Status](https://img.shields.io/badge/Focus-Power_Electronics_%7C_FEA_%7C_Embedded-00f2fe?style=for-the-badge)](#)

<br/>

### 🌐 [**🇬🇧 English Profile**](#-about-me) &nbsp;&nbsp;|&nbsp;&nbsp; [**🇹🇷 Türkçe Profil Özeti**](#-turkce-profil-ozeti)

---

</div>

## 📌 Executive Summary

> **Muhammet Raşit Taflan** is a senior Electrical and Electronics Engineering undergraduate at **Karadeniz Technical University (KTU)**, specializing in **Power Electronics & Conversion**, **Electromagnetic Finite Element Analysis (FEA)**, **Embedded Systems**, and **Closed-Loop Control Dynamics**.
> 
> His engineering methodology centers on bridging rigorous numerical physics modeling (Ansys Maxwell, MATLAB/Simulink) with physical hardware implementation, laboratory testing, and embedded control.

---

## 🧭 Core Engineering Pillars

```
+---------------------------------------------------------------------------------------------------------+
|                                    ENGINEERING COMPETENCY DOMAINS                                       |
+------------------------------------+------------------------------------+-------------------------------+
|  ⚡ Power Electronics & Conversion  |  🧲 Electromagnetic FEA & Maglev   |  🎯 Control Systems & Embedded |
|  • SMPS Topologies (Buck/Boost/Fly)|  • Ansys Maxwell 2D/3D Magnetostatics|  • Closed-Loop PID + Anti-Windup|
|  • LLC Resonant & PSFB (ZVS)       |  • FEMM Numerical Modeling         |  • Nonlinear Plant Dynamics   |
|  • Vienna PFC & Interleaved Boost  |  • B-H Saturation & Flux Density   |  • STM32 (ARM Cortex-M) C/C++ |
|  • Magnetics & Inductor Design     |  • Force vs. Air Gap Mapping       |  • CAN Bus, UART, ADC & Timers|
|  • Thermal Loss & Stress Analysis  |  • TÜBİTAK 2209-B Maglev Research  |  • Hardware Lab Test & Bench  |
+------------------------------------+------------------------------------+-------------------------------+
```

---

## 💼 Engineering Experience & Leadership

### ⚡ Hardware R&D Engineering Intern — Electric Vehicle Charging Systems
**Vestel R&D** • *Summer 2026 (6-Week Intensive R&D Internship)*  
* **Technical Focus:** Hardware architecture and power converter topology analysis for next-generation Electric Vehicle (EV) charging stations.
* **Converter Topologies:** Investigated high-efficiency isolated DC-DC stages including **LLC Resonant Converters** and **Phase-Shifted Full-Bridge (PSFB)** with Zero-Voltage Switching (ZVS), as well as **Vienna PFC** and **interleaved boost** input stages.
* **Laboratory & Validation:** Participated in power stage stress calculations, thermal characterization, component selection, CAN bus communication verification, and high-power laboratory instrumentation.

---

### 🏎️ Team Captain — Electric Race Vehicle Development
**Ege University Electric Vehicle Team** • *August 2023 – September 2024*  
* **Leadership & Architecture:** Directed the multidisciplinary engineering team through design, integration, and track testing of an efficiency-focused electric competition vehicle.
* **Electrical Powertrain & Low-Voltage:** Oversaw battery management system (BMS) integration, telemetry transmission, motor controller interfacing, and safety shutdown interlocks.
* **Milestone Execution:** Coordinated subsystem leads across powertrain, aerodynamics, mechanical chassis, and telemetry, ensuring technical compliance and race readiness.

---

### 🚝 Hyperloop Subsystem Engineering
**Hyperloop R&D Team** • *2024 – Present (Active)*  
* **Subsystem Focus:** Electromagnetic levitation actuators, linear propulsion dynamics, power distribution, and dynamic stabilization.
* **Integration:** Coupling finite element electromagnetic analysis with embedded sensors and real-time electronic drive circuitry for pod levitation stability.

---

## 🔬 Research & Academic Projects

### 🧲 TÜBİTAK 2209-B — PID-Controlled Electromagnetic Levitation System for Hyperloop Applications
> *Industry-Oriented Undergraduate Research Project Support Program (TÜBİTAK 2209-B)*  
> **Role:** Project Lead / Magnetic FEA & Hardware Design • **Institution:** Karadeniz Technical University

* **Electromagnetic Design & FEA:** Modeled cylindrical and U-core electromagnetic actuators in **Ansys Maxwell 2D Axisymmetric and 3D** environments. Executed adaptive mesh convergence studies and B-H non-linear core saturation analysis ($B_{sat} \approx 1.8\text{ T}$).
* **Verified Numerical Findings:**
  * **V1 Single Cylindrical Actuator ($r = 5\text{ mm}, L = 30\text{ mm}$):** Achieved **$0.4823\text{ N}$** lifting force at $4.8\text{ A}$ excitation current across a target **$5.0\text{ mm}$ working air gap** ($22.26\text{ mN}$ at $1.0\text{ A}$).
  * **V2 Pod Array Target:** Research specification for a multi-actuator distributed pod suspension aiming for **$\ge 130\text{ N}$**.
* **System Dynamics & Control:** Extracted non-linear force-current-distance look-up matrices into **MATLAB/Simulink**; designed a closed-loop **PID + Anti-Windup** position regulator verified under 300-second thermal endurance runs and external mechanical disturbance steps.
* 🔗 **Repository:** [`rasittaflan/Electromagnetic-Levitation-FEA-Simulations`](https://github.com/rasittaflan/Electromagnetic-Levitation-FEA-Simulations)  
* 🚀 **Interactive Studio:** [Launch 3D WebGL Maglev Digital Twin](https://rasittaflan.github.io/Electromagnetic-Levitation-FEA-Simulations/) | [Live Calculation Studio](https://rasittaflan.github.io/Electromagnetic-Levitation-FEA-Simulations/Maglev_Canli_Hesaplayici.html)

---

### ☀️ Interdisciplinary Engineering Capstone — Bodrum Gulet Hybrid Power & Smart EMS Optimization
> *KTÜ MHN 4001 Interdisciplinary Engineering Design*  
> **Authors:** Muhammet Raşit Taflan & Muhammed Emin Kadirov • **Department:** KTÜ EEE

* **Problem Formulation:** Traditional wooden Bodrum gulets (20–35 m) run continuous auxiliary diesel alternators 24 hours/day for hotel electrical loads, causing fuel waste, noise, soot, and marine emissions.
* **Engineered Architecture:** Integrated marine solar arrays (comparing **Model A: 8.0 kWp Fixed Bimini** vs. **Model B: 13.6 kWp Retractable Solar Wings**), **40 kWh LiFePO4 battery storage** ($28\text{ kWh}$ usable), and a **20 kW / 25 kVA auxiliary diesel generator** with a 30% wet-stacking prevention threshold.
* **Real-Time FSM Energy Management:** Built a discrete-time Finite State Machine (FSM) enforcing instantaneous Kirchhoff power balance across a 48 VDC bus ($\Delta t = 5\text{ min}$, $|P_{balance}| < 10^{-9}\text{ kW}$).
* **Validated Impact:**
  * **Fuel Savings:** Reduced daily consumption by **71.6%** (from $88.42\text{ L/day}$ down to $25.10\text{ L/day}$).
  * **Silent Operation:** Enabled **17.6 hours of continuous zero-emission silent anchoring** daily.
  * **Naval Stability:** Verified transverse metacentric height ($GM = 1.021\text{ m}$, $\Delta KG = +9.4\text{ mm}$), confirming hull form stability.
* 🔗 **Repository:** [`rasittaflan/Bodrum-Gulet-Hybrid-EMS-Simulator`](https://github.com/rasittaflan/Bodrum-Gulet-Hybrid-EMS-Simulator)  
* 🚀 **Interactive Simulation:** [Launch Live WebGL Gulet EMS Simulator](https://rasittaflan.github.io/Bodrum-Gulet-Hybrid-EMS-Simulator/)

---

## 🛠️ Featured Open-Source Engineering Suites

<table>
  <tr>
    <td width="33%" valign="top">
      <h3 align="center">🧲 Maglev FEA Suite</h3>
      <p align="center">
        <a href="https://github.com/rasittaflan/Electromagnetic-Levitation-FEA-Simulations">
          <img src="https://raw.githubusercontent.com/rasittaflan/Electromagnetic-Levitation-FEA-Simulations/main/assets/banner.svg" alt="Maglev FEA Suite" width="100%"/>
        </a>
      </p>
      <p><strong>TÜBİTAK 2209-B Electromagnetic Levitation & Control Suite:</strong></p>
      <ul>
        <li>Ansys Maxwell 2D/3D magnetostatic models.</li>
        <li>Mesh convergence & B-H saturation curves.</li>
        <li>Simulink PID + anti-windup closed-loop control.</li>
        <li>Interactive 3D Three.js digital twin.</li>
      </ul>
      <p>
        <a href="https://github.com/rasittaflan/Electromagnetic-Levitation-FEA-Simulations">📂 <strong>GitHub Repository</strong></a><br/>
        <a href="https://rasittaflan.github.io/Electromagnetic-Levitation-FEA-Simulations/">🚀 <strong>Launch 3D Studio</strong></a><br/>
        <a href="https://rasittaflan.github.io/Electromagnetic-Levitation-FEA-Simulations/Maglev_Canli_Hesaplayici.html">⚡ <strong>Live Force Calculator</strong></a>
      </p>
      <p><code>Ansys Maxwell</code> <code>Simulink</code> <code>Three.js</code> <code>PID</code></p>
    </td>
    <td width="33%" valign="top">
      <h3 align="center">⚡ Power Electronics Suite</h3>
      <p align="center">
        <a href="https://github.com/rasittaflan/Power_Electronics">
          <img src="https://raw.githubusercontent.com/rasittaflan/Power_Electronics/main/assets/banner.svg" alt="Power Electronics Suite" width="100%"/>
        </a>
      </p>
      <p><strong>16 SMPS Topologies Design & Live Formula Suite:</strong></p>
      <ul>
        <li>Based on Texas Instruments SLYU036A & SLYW038B.</li>
        <li>16 converters (Buck, Boost, PSFB, LLC, Flyback, Forward).</li>
        <li>400 live engineering equations cross-verified.</li>
        <li>100% offline interactive studio + Excel/Calc engines.</li>
      </ul>
      <p>
        <a href="https://github.com/rasittaflan/Power_Electronics">📂 <strong>GitHub Repository</strong></a><br/>
        <a href="https://raw.githack.com/rasittaflan/Power_Electronics/main/TI_16_Canli_Hesaplayici.html">🚀 <strong>Launch Live Calculator</strong></a><br/>
        <a href="https://raw.githack.com/rasittaflan/Power_Electronics/main/TI_16_Guc_Kaynagi_Topolojisi_Interaktif_Tablo.html">📊 <strong>Launch LaTeX Table</strong></a>
      </p>
      <p><code>SMPS</code> <code>DC-DC Topologies</code> <code>MathML</code> <code>Calc</code></p>
    </td>
    <td width="33%" valign="top">
      <h3 align="center">☀️ Marine Hybrid EMS</h3>
      <p align="center">
        <a href="https://github.com/rasittaflan/Bodrum-Gulet-Hybrid-EMS-Simulator">
          <img src="https://raw.githubusercontent.com/rasittaflan/Bodrum-Gulet-Hybrid-EMS-Simulator/main/screenshots/simulation_dashboard_preview.svg" alt="Bodrum Gulet EMS" width="100%"/>
        </a>
      </p>
      <p><strong>Bodrum Gulet Hybrid Renewable EMS Simulator:</strong></p>
      <ul>
        <li>Discrete FSM energy balance ($|P_{err}| < 10^{-9}\text{ kW}$).</li>
        <li>13.6 kWp folding solar wings vs. 8.0 kWp bimini.</li>
        <li>71.6% diesel fuel reduction verified.</li>
        <li>Dynamic 3D ocean hydrodynamics & stability.</li>
      </ul>
      <p>
        <a href="https://github.com/rasittaflan/Bodrum-Gulet-Hybrid-EMS-Simulator">📂 <strong>GitHub Repository</strong></a><br/>
        <a href="https://rasittaflan.github.io/Bodrum-Gulet-Hybrid-EMS-Simulator/">🚀 <strong>Launch Live Simulation</strong></a>
      </p>
      <p><code>Hybrid EMS</code> <code>FSM</code> <code>LiFePO4</code> <code>Hydrodynamics</code></p>
    </td>
  </tr>
</table>

---

## 🧰 Technical Skills & Engineering Toolchain

| Discipline / Domain | Tools & Technologies | Engineering Application |
| :--- | :--- | :--- |
| **Simulation & FEA** | `Ansys Maxwell (2D/3D)`, `FEMM`, `MATLAB / Simulink`, `Simscape` | Electromagnetic actuator modeling, flux density saturation ($B$-$H$), closed-loop control dynamics, plant linearization. |
| **Power Electronics** | `DC-DC Topologies`, `LLC Resonant`, `PSFB (ZVS)`, `Vienna PFC`, `Flyback/Forward` | High-efficiency converter calculation, inductor/transformer magnetics design, semiconductor stress & thermal evaluation. |
| **Embedded & Firmware** | `STM32 (ARM Cortex-M)`, `STM32CubeIDE`, `C`, `C++` | Bare-metal & HAL firmware development, interrupt service routines, timer-triggered PWM, ADC sampling. |
| **Communication & Protocols** | `CAN Bus`, `UART`, `SPI`, `I2C` | Automotive & industrial telemetry, sensor data acquisition, powertrain module communication. |
| **Laboratory & Hardware Testing** | `Digital Storage Oscilloscopes`, `Power Analyzers`, `Electronic Loads`, `LCR Meters` | Real-time waveform debugging, voltage/current ripple measurement, thermal verification, bench testing. |
| **Mathematical Modeling** | `MATLAB`, `Python (NumPy / SciPy)`, `Excel / Calc Formula Engines`, `LaTeX` | Discrete energy balance, non-linear lookup mapping, analytical converter equations, mathematical documentation. |
| **Development & Workflow** | `Git`, `GitHub`, `VS Code`, `Three.js / WebGL`, `HTML5 / CSS / JS` | SCM version control, engineering documentation, interactive digital twin simulators. |

---

## 📊 GitHub Engineering Activity

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=rasittaflan&show_icons=true&theme=tokyonight&hide_border=false&bg_color=0b1329&title_color=38bdf8&text_color=94a3b8&icon_color=00f2fe&border_color=1e293b" alt="Rasit Taflan GitHub Stats" height="165" />
&nbsp;
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=rasittaflan&layout=compact&theme=tokyonight&hide_border=false&bg_color=0b1329&title_color=38bdf8&text_color=94a3b8&border_color=1e293b" alt="Top Languages" height="165" />

</div>

---

<a id="turkce-profil-ozeti"></a>

## 🇹🇷 Türkçe Profil Özeti

<details>
<summary><b>🔍 Türkçe Mühendislik Özeti ve Proje Detaylarını Görüntülemek İçin Tıklayın</b></summary>
<br/>

### Hakkımda
**Muhammet Raşit Taflan**, Karadeniz Teknik Üniversitesi (KTÜ) Elektrik-Elektronik Mühendisliği 4. sınıf lisans öğrencisidir. Başlıca çalışma alanları:
* **Güç Elektroniği ve Güç Dönüşümü:** DC-DC dönüştürücü topolojileri (Buck, Boost, Flyback, Forward, Köprü topolojileri), LLC rezonans dönüştürücüler, Faz Kaydırmalı Tam Köprü (PSFB - ZVS), Vienna PFC, endüktör ve manyetik bileşen tasarımı.
* **Sonlu Elemanlar Analizi (FEA) ve Elektromanyetik Simülasyon:** Ansys Maxwell 2D/3D ve FEMM ortamlarında manyetik akı yoğunluğu, B-H doyumu, hava aralığı ve manyetik kuvvet haritalama.
* **Gömülü Sistemler ve Kontrol Dinamiği:** STM32 (ARM Cortex-M) mikrodenetleyiciler, C/C++ gömülü yazılım geliştirme, kapalı çevrim PID ve anti-windup denetim algoritmaları, CAN bus, UART, ADC ve PWM çevre birimleri.
* **Yenilenebilir Enerji ve Hibrit Sistemler:** Güneş PV, batarya depolama ve jeneratör tabanlı akıllı enerji yönetim sistemleri (EMS).

---

### Mühendislik ve Ar-Ge Deneyimleri
1. **Vestel Ar-Ge (2026 Yaz Stajı — Donanım Tasarımı):**
   * Elektrikli araç şarj istasyonlarının güç katı donanım tasarımı üzerine 6 haftalık yoğun Ar-Ge stajı.
   * LLC rezonans, PSFB, Vienna PFC, interleaved boost topolojileri, güç bileşenleri termal stres analizleri ve laboratuvar ölçümleri.
2. **Ege Üniversitesi Elektrikli Araç Takımı (Ağustos 2023 – Eylül 2024 — Takım Kaptanı):**
   * Verimlilik odaklı elektrikli yarış aracının batarya yönetim sistemi, telemetri, motor sürücü entegrasyonu ve teknik yarış regülasyonlarına uyum süreçlerinin yönetimi.
3. **Hyperloop Takım Çalışmaları (2024 – Aktif):**
   * Elektromanyetik levitasyon, itki dinamikleri ve araç stabilite sistemleri üzerine elektronik donanım çalışmaları.
4. **TÜBİTAK 2209-B Üniversite-Sanayi İş Birlikli Araştırma Projesi (Proje Yürütücüsü):**
   * *"PID Kontrollü Elektromanyetik Levitasyon Sistemi Tasarımı ve Hyperloop Uygulamalarına Entegrasyonu"*.
   * Ansys Maxwell 2D/3D magnetostatik FEA analizleri ile 5 mm hava aralığında $0.4823\text{ N}$ @ $4.8\text{ A}$ V1 aktüatör kuvvet doğrulaması ve MATLAB/Simulink kapalı çevrim PID denetleyici tasarımı.
5. **Disiplinlerarası Mühendislik Tasarımı (KTÜ MHN 4001):**
   * *"Bodrum Guletlerinde Yenilenebilir Enerji Destekli Hibrit Güç ve Akıllı Enerji Yönetim Sistemi Optimizasyonu"*.
   * 48 VDC bara üzerinde anlık güç dengesini sağlayan sonlu durum makinesi (FSM) tabanlı EMS tasarımı; %71.6 yakıt tasarrufu ve günlük 17.6 saat sessiz çalışma modunun doğrulanması.

</details>

---

## 📬 Connect With Me / İletişim

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect_on_LinkedIn-0077b5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rasittaflan)
[![GitHub](https://img.shields.io/badge/GitHub-Follow_on_GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/rasittaflan)

<br/>

```
Muhammet Raşit Taflan
Department of Electrical and Electronics Engineering
Karadeniz Technical University (KTU) | Trabzon, Türkiye
LinkedIn: https://www.linkedin.com/in/rasittaflan
GitHub:   https://github.com/rasittaflan
```

---

*Engineered with precision, rigorous physics simulation, and dedication to R&D excellence ⚡*

</div>
