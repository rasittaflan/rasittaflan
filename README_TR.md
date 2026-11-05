<div align="center">

<img src="./assets/profile_banner.svg" alt="Muhammet Raşit Taflan — Mühendislik Portföyü Afişi" width="100%" />

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-rasittaflan-0077b5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rasittaflan)
[![GitHub](https://img.shields.io/badge/GitHub-rasittaflan-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/rasittaflan)
[![Kurum](https://img.shields.io/badge/KTÜ-Elektrik--Elektronik_Mühendisliği-0284c7?style=flat-square&logo=mortarboard&logoColor=white)](https://www.ktu.edu.tr/eee)

<br/>

**[Genel Bakış](#1-genel-tanitim--muhendislik-yaklasimi)** &nbsp;|&nbsp; **[Öne Çıkan Projeler](#2-one-cikan-muhendislik-projeleri)** &nbsp;|&nbsp; **[Deneyimler](#3-arastirma-ve-muhendislik-deneyimleri)** &nbsp;|&nbsp; **[Teknik Yetkinlikler](#4-teknik-yetkinlikler)** &nbsp;|&nbsp; **[Switch to English (README.md)](README.md)**

</div>

---

<a id="genel-bakis"></a>

## 1. Genel Tanıtım & Mühendislik Yaklaşımı

Karadeniz Teknik Üniversitesi (KTÜ) **Elektrik-Elektronik Mühendisliği 4. sınıf lisans öğrencisiyim** (*Beklenen Mezuniyet: 2027*).

Mühendislik çalışmalarım; soyut yazılım geliştirmekten ziyade **sayısal çoklu fizik modellemesi**, **güç dönüştürücü topolojileri** ve **gömülü kapalı çevrim denetim** yöntemlerini birleştirerek fiziksel mühendislik problemlerini çözmeye odaklanmaktadır:

* **Güç Elektroniği ve Güç Dönüşümü:** Anahtarlamalı DC-DC dönüştürücüler (Buck, Boost, LLC Rezonans, Faz Kaydırmalı Tam Köprü PSFB - ZVS, Vienna PFC), manyetik bileşen tasarımı, yarıiletken gerilim/akım stres analizleri ve termal modelleme.
* **Sonlu Elemanlar Analizi (FEA) ve Manyetik Simülasyon:** Ansys Maxwell 2D ve FEMM ortamlarında magnetostatik analizler; hava aralığı manyetik akı yoğunluğu, B-H eğrisi doyumu ve kuvvet hesaplamaları.
* **Kontrol Sistemleri ve Dinamik:** Doğrusal olmayan sistem modelleme, ayrık zamanlı durum geri beslemesi ve MATLAB/Simulink ortamında PID + Anti-Windup algoritmaları.
* **Gömülü Sistemler ve Donanım:** ARM Cortex-M mimarili mikrodenetleyiciler üzerinde (**Nuvoton M032KG** ve **STM32**) C ile bare-metal geliştirme, donanımsal zamanlayıcı PWM üretimi, çok kanallı ADC örnekleme ve UART/CAN telemetrisi.

---

<a id="one-cikan-projeler"></a>

## 2. Öne Çıkan Mühendislik Projeleri

Aşağıda listelenen tüm projeler; kaynak kodları, simülasyon modelleri ve doğrulanabilir analitik hesaplama tablolarıyla sunulmuştur.

---

### Proje 1: Elektromanyetik Levitasyon (Maglev) FEA ve Sistem Dinamiği Paketi
> **TÜBİTAK 2209-B Sanayiye Yönelik Lisans Araştırma Projeleri Destekleme Programı**  
> *Karadeniz Teknik Üniversitesi — Elektrik-Elektronik Mühendisliği Bölümü*

* **Mühendislik Problemi:** Yüksek hızlı kara taşımacılığı (Hyperloop) ve endüstriyel temassız konumlandırmada kullanılan elektromanyetik askılama sistemleri, Earnshaw Teoremi gereği açık çevrimde kararsızdır. Kaldırma kuvveti hava aralığının karesiyle ters orantılı ($F \propto 1/g^2$) olduğundan sistem yüksek derecede doğrusal olmayan fiziksel dinamik sergiler.
* **Teknik Yaklaşım:** **Ansys Maxwell 2D Eksenel Simetrik** magnetostatik sonlu elemanlar analizi (FEA) ile **MATLAB/Simulink** kapalı çevrim geri beslemeli denetim tasarımını birleştiren bir iş akışı uygulanmıştır.
* **Gerçekleme:**
  * Steel 1008 çelik nüveli ($r = 5\text{ mm}, L = 30\text{ mm}$) ve 500 tur bakır sargılı ($d = 0.7\text{ mm}$) silindirik elektromıknatıs geometrisi modellenmiştir.
  * Ansys Maxwell magnetostatik çözücüsünde adaptif mesh adımları %1.0 hedef hata kriteriyle yürütülmüştür.
  * Doğrusal olmayan sistem dinamikleri MATLAB/Simulink ortamında modellenmiş; ayrık zamanlı PID + Anti-Windup konum regülatörü ve ısıl sınırlar test edilmiştir.
* **Sonuçlar ve Doğrulama Durumu:**
  * *FEA Simülasyon Sonucu (V1 Aktüatör):* Ansys Maxwell 2D magnetostatik analizinde, **$5.0\text{ mm}$ hava aralığında** $1.0\text{ A}$ nominal akımda dikey kaldırma kuvveti **$F_z = 22.26\text{ mN}$** ($4.8\text{ A}$ akımda $F_z \approx 0.482\text{ N}$) olarak hesaplanmıştır.
  * *Dinamik Simülasyon Durumu:* Simulink ortamında 300 saniyelik sürekli çalışma ve basamak bozucu testleri altında kapalı çevrim kararlılık simülasyonla doğrulanmıştır.
  * *Tasarım Hedefi:* V2 geliştirme aşaması için araç süspansiyonuna yönelik çoklu aktüatör dizisinde hedef $\ge 130\text{ N}$ olarak belirlenmiştir.
* 📂 **Depo:** [`rasittaflan/Electromagnetic-Levitation-FEA-Simulations`](https://github.com/rasittaflan/Electromagnetic-Levitation-FEA-Simulations)
* 🚀 **Canlı Demo:** [3B WebGL Maglev Dijital İkizi](https://rasittaflan.github.io/Electromagnetic-Levitation-FEA-Simulations/) | [Canlı Kuvvet Hesaplayıcı](https://rasittaflan.github.io/Electromagnetic-Levitation-FEA-Simulations/Maglev_Canli_Hesaplayici.html)

---

### Proje 2: Güç Elektroniği — 16 SMPS Topolojisi Tasarım ve Canlı Formül Paketi
> **Texas Instruments Standartlarına Dayalı Mühendislik Hesaplama Motoru (SLYU036A & SLYW038B)**

* **Mühendislik Problemi:** Farklı gerilim oranlarına sahip güç kaynaklarında 16 yalıtımlı ve yalıtımsız topolojinin yarıiletken stresleri, görev periyodu (duty cycle) ve sürekli/kesintili iletim modları (CCM/DCM) açısından karşılaştırılması ve boyutlandırılması gerekmektedir.
* **Teknik Yaklaşım:** Elektronik tablo motorları (`.xlsx` ve `.ods`) ile sıfır bağımlılıklı tarayıcı tabanlı analitik motorları eşleyen çift yönlü doğrulanmış bir hesaplama paketi geliştirilmiştir.
* **Gerçekleme:**
  * 16 temel SMPS topolojisi sentezlenmiştir (Buck, Boost, Inverting Buck-Boost, SEPIC, Ćuk, Zeta, Flyback, Two-Switch Flyback, Active Clamp Forward, Single-Switch Forward, Two-Switch Forward, Push-Pull, Weinberg, Half-Bridge, Full-Bridge ve Phase-Shifted Full-Bridge PSFB - ZVS).
  * 14 kullanıcı giriş parametresini dönüştürücü başına 25 çıkış değişkenine bağlayan analitik hesaplama omurgası kurulmuştur.
* **Sonuçlar ve Doğrulama Durumu:**
  * *Analitik Eşlik:* Excel/Calc modelleri ile web hesaplama motoru arasında 1:1 sayısal eşliği sağlanan **400 aktif mühendislik denklemi** formüle edilmiştir.
  * *Model Tabanlı Hesaplamalar:* Endüktör akım dalgalanması ($\Delta I_L$), çıkış gerilim dalgalanması ($\Delta V_{out}$), tepe yarıiletken stresleri ve Sıfır Gerilimde Anahtarlama (ZVS) koşulları analitik olarak hesaplanmaktadır.
* 📂 **Depo:** [`rasittaflan/Power_Electronics`](https://github.com/rasittaflan/Power_Electronics)
* 🚀 **Canlı Demo:** [Canlı SMPS Hesaplayıcı Stüdyosu](https://raw.githack.com/rasittaflan/Power_Electronics/main/TI_16_Canli_Hesaplayici.html) | [İnteraktif LaTeX Referans Tablosu](https://raw.githack.com/rasittaflan/Power_Electronics/main/TI_16_Guc_Kaynagi_Topolojisi_Interaktif_Tablo.html)

---

### Proje 3: Bodrum Gulet Hibrit EMS — Yenilenebilir Güç ve Gemi Stabilitesi Optimizasyonu
> **KTÜ MHN 4001 Disiplinlerarası Mühendislik Tasarımı Bitirme Projesi**  
> *Yazarlar: Muhammet Raşit Taflan & Muhammed Emin Kadirov*

* **Mühendislik Problemi:** Bodrum ahşap guletlerinde (20–35 m) koyda demirleme esnasında otel yüklerini beslemek amacıyla 24 saat kesintisiz çalışan yardımcı dizel alternatörler; yüksek yakıt tüketimi, akustik gürültü ve kıyı deniz kirliliğine yol açmaktadır.
* **Teknik Yaklaşım:** Marin güneş PV, lityum batarya ve yardımcı dizel jeneratörden oluşan mikroşebeke modellenmiş; sonlu durum makinesi (FSM) tabanlı akıllı enerji yönetimi (EMS) tasarlanırken gemi enine stabilitesi doğrulanmıştır.
* **Gerçekleme:**
  * 48 VDC dağıtım barasında anlık Kirchhoff güç dengesini sağlayan ayrık zamanlı FSM geliştirilmiştir ($\Delta t = 5\text{ dk}$, denge toleransı $|P_{denge}| < 10^{-9}\text{ kW}$).
  * Bodrum koordinatları ($37.034^\circ\text{ K}, 27.430^\circ\text{ D}$) için astronomik güneş izleme algoritması kurulmuş; **Model A (8.0 kWp Sabit Bimini)** ile **Model B (13.6 kWp Açılır Kapanır Güneş Kanatları)** rüzgar kilitleri altında karşılaştırılmıştır.
* **Sonuçlar ve Doğrulama Durumu:**
  * *Simülasyon Tahmini:* Günlük dizel tüketiminde **%71.6 yakıt tasarrufu** ($88.42\text{ L/gün}$'den $25.10\text{ L/gün}$'e düşüş) simüle edilmiştir.
  * *İşletme Tahmini:* Jeneratör çalışma süresi günde 24.0 saatten 6.4 saate indirilerek günlük **17.6 saat sessiz seyir modu** öngörülmüştür.
  * *Analitik Projeksiyon:* 120 günlük standart sezon boyunca **20.36 ton $\mathrm{CO}_2$ salımının engelleneceği** hesaplanmıştır.
  * *Ön Hidrostatik Hesaplama:* Enine metasentrik yükseklik ($GM = 1.021\text{ m}$, $\Delta KG = +9.4\text{ mm}$) hesaplanarak tekne form dengesi kontrol edilmiştir.
* 📂 **Depo:** [`rasittaflan/Bodrum-Gulet-Hybrid-EMS-Simulator`](https://github.com/rasittaflan/Bodrum-Gulet-Hybrid-EMS-Simulator)
* 🚀 **Canlı Demo:** [3B WebGL Gulet EMS Simülatörü](https://rasittaflan.github.io/Bodrum-Gulet-Hybrid-EMS-Simulator/)

---

<a id="deneyimler"></a>

## 3. Araştırma ve Mühendislik Deneyimleri

### ⚡ Vestel Ar-Ge — Donanım Tasarımı Stajyeri
**Elektrikli Araç Şarj Sistemleri** • *2026 Yaz Dönemi (6 Haftalık Donanım Ar-Ge Stajı)*  
* Elektrikli araç şarj istasyonlarının güç dönüştürücü mimarisi kapsamında **LLC Rezonans Dönüştürücü** ve Sıfır Gerilimde Anahtarlamalı (ZVS) **Faz Kaydırmalı Tam Köprü (PSFB)** topolojileri incelendi.
* Üç fazlı **Vienna PFC** doğrultucu ve **interleaved boost** katlarının güç faktörü düzeltimi ve harmonik azaltımı analiz edildi.
* Yüksek güçlü laboratuvar ortamında yarıiletken güç kayıp hesaplamaları, kondansatör dalgalanma akımı bütçesi, termal stres testleri ve CAN bus telemetri analizleri yürütüldü.

---

### 🧲 TÜBİTAK 2209-B — Lisans Araştırma Projesi
**Elektromanyetik Levitasyon ve Kontrol** • *Karadeniz Teknik Üniversitesi*  
* *Proje Başlığı:* "PID Kontrollü Elektromanyetik Levitasyon Sistemi Tasarımı ve Hyperloop Uygulamalarına Entegrasyonu".
* 2D magnetostatik sonlu elemanlar analizi, hava aralığı akı hesaplamaları ve bobin termal dağılım modellemesi yürütüldü.
* Ansys Maxwell simülasyon verilerini Simulink dinamik sistem modelleriyle birleştiren ayrık zamanlı kapalı çevrim geri besleme algoritmaları geliştirildi.

---

### 🏎️ Ege Üniversitesi Elektrikli Araç Takımı — Eski Takım Kaptanı
**Elektrikli Yarış Aracı Mühendisliği** • *Ağustos 2023 – Eylül 2024*  
* Verimlilik odaklı elektrikli yarış aracının tasarımı, bileşen entegrasyonu, düşük gerilim kablo demeti montajı ve pist testleri süreçlerinde öğrenci mühendislik ekibine liderlik yapıldı.
* Batarya Yönetim Sistemi (BMS) hücre izleme, yüksek gerilim güvenlik kilitleri, motor sürücü parametre ayarları ve CAN telemetri sistemleri yönetildi.
* Teknik yarış regülasyonlarına ve elektriksel güvenlik standartlarına tam uyum sağlandı.

---

### 🚝 Hyperloop Takımı Mühendislik Çalışmaları
**Levitasyon ve Dinamik Alt Sistemleri**  
* Elektromanyetik levitasyon aktüatörleri, doğrusal indüksiyon itki konseptleri, güç dağıtımı ve dinamik stabilite alt sistemlerinde donanım geliştirme çalışmalarına katkı sağlandı.

---

<a id="teknik-yetkinlikler"></a>

## 4. Teknik Yetkinlikler

| Yetkinlik Alanı | Temel Araçlar ve Çatılar | Pratik Mühendislik Uygulaması |
| :--- | :--- | :--- |
| **Güç Elektroniği** | DC-DC Dönüştürücüler, LLC Rezonans, PSFB (ZVS), Vienna PFC, Buck/Boost Topolojileri | Dönüştürücü tasarımı, manyetik nüve/endüktör hesabı, yarıiletken gerilim/akım stres ve termal kayıp analizi. |
| **Kontrol ve Simülasyon** | MATLAB, Simulink, Simscape, Durum Uzayı, Klasik Denetim | Doğrusal olmayan dinamik sistem modelleme, ayrık zamanlı PID + Anti-Windup denetimi, kararlılık analizleri. |
| **Elektromanyetizma & FEA** | Ansys Maxwell 2D, FEMM 4.2 | 2D magnetostatik alan analizi, B-H doyum modellemesi, bobin endüktans hesabı, hava aralığı kuvvet haritalama. |
| **Gömülü Sistemler** | **Nuvoton M032KG** (ARM Cortex-M0), **STM32** (ARM Cortex-M), C, GCC, VS Code, Nu-Link, STM32CubeIDE | Bare-metal gömülü yazılım, donanımsal zamanlayıcı PWM üretimi, çok kanallı ADC örnekleme, UART iletişimi, CAN bus. |
| **Mühendislik Yazılımları** | Python (NumPy / SciPy), JavaScript, HTML5 / MathML, LaTeX, Git, GitHub | Ayrık sayısal modelleme, etkileşimli hesaplama motorları, sürüm takibi, teknik dokümantasyon. |
| **Laboratuvar Ekipmanları** | Dijital Hafızalı Osiloskop, Güç Analizörü, Elektronik Yük, LCR Metre | Güç katı dalga formu analizi, akım dalgalanması ölçümü, termal testler ve tezgah doğrulaması. |

---

<a id="egitim"></a>

## 5. Eğitim ve Akademik Geçmiş

* **Lisans Derecesi — Elektrik-Elektronik Mühendisliği**  
  **Karadeniz Teknik Üniversitesi (KTÜ)**, Trabzon, Türkiye  
  *Durum:* 4. Sınıf Lisans Öğrencisi &nbsp;|&nbsp; *Beklenen Mezuniyet:* **2027**  
  *İlgili Dersler:* Güç Elektroniği, Kontrol Sistemleri, Elektromanyetik Alan Teorisi, Mikroişlemciler, Elektrik Makineleri, Sinyaller ve Sistemler.

---

<a id="iletisim"></a>

## 6. İletişim & Profesyonel Bağlantılar

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-LinkedIn'de_Bağlantı_Kur-0077b5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rasittaflan)
[![GitHub](https://img.shields.io/badge/GitHub-GitHub'da_Takip_Et-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/rasittaflan)

<br/>

```
Muhammet Raşit Taflan
Elektrik-Elektronik Mühendisliği Bölümü
Karadeniz Teknik Üniversitesi (KTÜ) | Trabzon, Türkiye
LinkedIn: https://www.linkedin.com/in/rasittaflan
GitHub:   https://github.com/rasittaflan
```

---

*Disiplinli mühendislik analizi, fiziksel simülasyon ve araştırmaya dayalı donanım tasarımı ⚡*

</div>
