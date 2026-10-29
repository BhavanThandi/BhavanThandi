<div align="center">

<img src="https://i.pinimg.com/originals/6d/77/38/6d773843a8b38d03aa06e6144b51382d.gif" width="420px" />

# Bhavan Thandi

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=9B59B6&center=true&vCenter=true&width=500&lines=SFU+Engineering+%7C+Systems;Builder+of+things+that+actually+work;C%2B%2B+%7C+Python+%7C+Arduino+%7C+CAD" alt="Typing SVG" />

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-bhavan--thandi-7D3C98?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/bhavan-thandi)
[![Email](https://img.shields.io/badge/Email-Bst9@sfu.ca-6C3483?style=for-the-badge&logo=gmail&logoColor=white)](mailto:Bst9@sfu.ca)
[![GitHub](https://img.shields.io/badge/GitHub-BhavanThandi-8E44AD?style=for-the-badge&logo=github&logoColor=white)](https://github.com/BhavanThandi)

</div>

---

## 🟣 About Me

I'm a third-year Engineering student at **Simon Fraser University** with a concentration in **Systems Engineering** and a **Beedie Luminaries Scholarship**. I'm drawn to projects that sit at the intersection of hardware and software — things you can hold, plug in, and actually watch work.

I enjoy designing systems from the ground up: from thermodynamic calculations and CAD models to microcontroller firmware and circuit assembly. If it involves building something that didn't exist before, I'm in.

**✨ Interests**
- Embedded systems and microcontroller programming
- Electronics design, PCB assembly, and circuit analysis
- CAD modelling and 3D printing for functional prototypes
- Writing clean, efficient low-level code in C and C++

---

## 💼 Current Experience

**Sales Associate / Technician — Sport Chek** *(August 2024 – Present)*
- Cross-trained across multiple departments, handling high-volume transactions and customer service simultaneously in a fast-paced retail environment
- Trained in the service department to build, fix, and tune sports equipment including bikes, snow gear, and rackets
- Resolved conflicts between coworkers and customers, consistently leaving both parties satisfied

**API Discovery — TeejLab** *(September 2022 – June 2023)*
- Researched and catalogued publicly available APIs from platforms like GitHub to grow TeejLab's API intelligence library
- Validated authentication tokens and organized APIs by category to improve searchability and client usability
- Gained hands-on experience with RESTful APIs, API documentation, and token-based authentication

---

## 🚀 Featured Projects

### 🥊 AttackIt — Instrumented Striking Target *(in progress)*
**Tech: Embedded C++ • ESP32 • PlatformIO • Analog Signal Conditioning • Python • WebSerial**

- Designing a wall-mounted striking target that measures impact force and strike location from a 7-channel piezoelectric sensor array, at a ~$148 CAD bill of materials against $1,500+ commercial alternatives
- Built a custom analog front end per channel — input clamping, peak-detect into a hold capacitor, and an RC discharge — then bench-tuned the capacitor and resistor 8x to move hand strikes from ADC clipping to ~1100 mV against a 3300 mV ceiling
- Implemented integer-only zone localization that scores the 7-channel voltage vector against spillover templates with a squared-cosine fit, avoiding floating point on the MCU
- Replaced a naive refractory timer with a hysteresis re-arm state machine plus a fault guard, eliminating ghost duplicate impact events
- Wrote a Python calibration pipeline that fits linear and power models, selects on RMSE, and emits a C++ header the firmware auto-detects, so recalibration needs no source edits
- Phase 1 validated on hardware; drop-test calibration rig in build

### 🤖 Self-Balancing Person-Following Robot *(in progress)*
**Tech: Embedded Linux • C++ • BeagleY-AI • Real-Time R5F Core • I2C • PID Control**

- Team lead on a 5-person ENSC 351 project building a two-wheeled balancing robot that detects a person, follows them at a set distance, and streams live video with clickable detection boxes to a browser
- Own the balance subsystem: fusing MPU6050 IMU and wheel encoder data with a complementary filter, and running a cascaded PID loop on the board's real-time R5F core
- Stabilizing the camera against the robot's own tilt by subtracting the measured angle from the commanded servo pitch, so the view stays level while the robot rocks
- Responsible for the chassis build, wiring, and the 3.3 V encoder level constraint that protects the board's GPIO

### 🔑 [PhoneKey: ESP32 BLE Phone-as-Key](https://github.com/BhavanThandi/ESP32-PhoneKey)
**Tech: Kotlin • Jetpack Compose • C++ • ESP32 • Bluetooth Low Energy • GATT**

- Built an Android app that unlocks an ESP32 over Bluetooth Low Energy, with the firmware owning the lock state and the phone acting only as a view onto it
- Chose confirmed UI over optimistic UI with a 3-second timeout, because a screen reading "unlocked" when the hardware did not act is a safety bug rather than a polish issue
- Paired notify-on-change with a read-on-connect, since BLE notifications are unacknowledged and one sent mid-connection is lost with no retransmission
- Diagnosed undocumented failures including a CCCD the ESP32 Arduino core does not auto-create, and Android manifest permissions that build clean but leave the app with none
- Built an in-app event log holding scan RSSI, discovery, subscription status, and raw GATT error codes, which became the primary debugging surface

### ⚡ [Edison — AI Agent for Breadboard Circuits](https://github.com/BhavanThandi/EDISON)
**Tech: Circuit Analysis • Modified Nodal Analysis • SPICE Methods • JavaScript** · [Live demo](https://edison-snowy.vercel.app)

- Built at StormHacks 2026 with two teammates: a 3D breadboard where an AI agent places parts and wires from a plain-English description, and a from-scratch simulator checks the build works
- Helped design the modified nodal analysis solver, the method SPICE is built on, where every component stamps its equations into one matrix solved for all node voltages at once
- Validated the simulator against real circuits on real parts, so simulated results matched what the bench actually did
- Contributed the circuit design and testing side, including op-amp behaviour at the supply rails

### 🫖 [Smart Mug: ICUP](https://github.com/BhavanThandi/Smart-Mug-ICUP)
**Tech: C++ • Arduino Pro Mini • MAX6675 Thermocouple • SSD1306 OLED • Li-ion**

- Designed and built a self-heating smart mug that monitors and regulates fluid temperature in real time, targeting a 35°C differential (25°C → 60°C) within 15 minutes
- Applied Q=mcΔt to calculate a required heating power of ~81.5W, selecting a 12V 50W heating rod driven through a MOSFET and controlled via thermocouple feedback
- Programmed an Arduino Pro Mini in C++ to handle temperature sensing, on/off heating control, button inputs, preset temperatures, and a live OLED display — all updating every 100ms
- Designed a full multi-part enclosure in Fusion 360 using PLA, ABS, and Nylon, with dedicated internal chambers for electronics, heating element, and a custom 6S Li-ion battery pack (30Wh+)
- Built the battery pack from 12x 18350 Li-ion cells managed by a 6S BMS, positioned at the bottom of the mug for a low centre of gravity

### 🚲 [Foldable Bike Design — UrbanGear Innovations](https://github.com/BhavanThandi/foldable-bike-frame)
**Tech: SolidWorks • Engineering Drawing • Assembly Mates**

- Designed and modeled a compact foldable bike frame for urban commuters in SolidWorks, individually creating parts including the frame, hinges, handlebars, seat clamp, wheels, and fastener hardware from scratch
- Evaluated three distinct folding mechanisms — mid-frame rotation, wheel pivot, and rod hinge — comparing structural strength and folding efficiency to select the optimal final design
- Assembled all components into a full SolidWorks assembly using concentric, coincident, and parallel mates to accurately simulate the bike's folding motion and part interactions
- Produced multi-view engineering drawings with proper dimensioning and orthographic projections for each custom part in accordance with technical drafting standards

---

## 🛠 Tech Stack

**Languages**

![C++](https://img.shields.io/badge/C++-6C3483?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![C](https://img.shields.io/badge/C-7D3C98?style=for-the-badge&logo=c&logoColor=white)
![Python](https://img.shields.io/badge/Python-8E44AD?style=for-the-badge&logo=python&logoColor=white)
![MATLAB](https://img.shields.io/badge/MATLAB-9B59B6?style=for-the-badge&logo=mathworks&logoColor=white)
![VHDL](https://img.shields.io/badge/VHDL-A569BD?style=for-the-badge&logoColor=white)
![R](https://img.shields.io/badge/R-BB8FCE?style=for-the-badge&logo=r&logoColor=white)

**Hardware & Tools**

![Arduino](https://img.shields.io/badge/Arduino-6C3483?style=for-the-badge&logo=arduino&logoColor=white)
![SolidWorks](https://img.shields.io/badge/SolidWorks-7D3C98?style=for-the-badge&logoColor=white)
![Fusion360](https://img.shields.io/badge/Fusion_360-8E44AD?style=for-the-badge&logo=autodesk&logoColor=white)
![Soldering](https://img.shields.io/badge/Soldering-9B59B6?style=for-the-badge&logoColor=white)
![Circuit Design](https://img.shields.io/badge/Circuit_Design-A569BD?style=for-the-badge&logoColor=white)
![3D Printing](https://img.shields.io/badge/3D_Printing-BB8FCE?style=for-the-badge&logoColor=white)

---

## 📌 Let's Connect

📩 Email: Bst9@sfu.ca
🐙 GitHub: github.com/BhavanThandi
💼 LinkedIn: linkedin.com/in/bhavan-thandi
