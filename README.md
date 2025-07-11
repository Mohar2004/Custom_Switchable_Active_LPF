# 🧠 Active Low-Pass Filter (LPF) Design and PCB Implementation

This repository contains the full design workflow for a **second-order active low-pass filter** (LPF) using the **Sallen-Key topology**, including:

- Circuit analysis and design
- LTspice simulations for frequency response and performance
- Altium schematic and PCB layout
- Switchable capacitor configuration to toggle between **Butterworth** and **Chebyshev** responses

---

## 🛠️ Project Overview

- **Filter Type**: Active Low-Pass Filter (2nd Order)
- **Topology**: Sallen-Key (unity gain)
- **Op-Amp Used**: OPA277UA
- **Corner Frequency**: 100 Hz
- **Two Modes**:  
  - Butterworth (Q ≈ 0.707)  
  - Chebyshev (Q ≈ 1.15)
- **Switching Mechanism**: Manual SPDT SMD switch (e.g., JS202011SCQN) to toggle between capacitor configurations

---

## 🔁 Features

- Accurate cutoff frequency using:
  - \( R = 10 \, \text{kΩ} \)
  - \( C = \sim 159 \, \text{nF} \) for 100 Hz
- Dual-mode filter: toggle between flat and sharp roll-off using switch
- Clean PCB design with surface-mount components
- Simulated in LTspice for frequency and transient response
- Schematic and PCB created in Altium Designer

---

## 📈 Simulation Results

- **Butterworth Response**:  
  - Q = 0.707  
  - Smooth roll-off  
  - Flat passband

- **Chebyshev Response**:  
  - Q ≈ 1.15  
  - Sharper roll-off  
  - Slight peak at cutoff

All plots and verification included in `/LTspice`.

---

## ⚙️ How to Use

1. Open `.asc` file in LTspice to simulate filter response
2. Toggle between capacitors using the SPDT switch to switch filter types
3. In Altium Designer:
   - Open `lpf_project.PrjPcb`
   - Review schematic and PCB layout
   - Use 3D view (`3` key in PCB view) for inspection
4. Use the provided BOM for surface-mount assembly

---

## 🧰 Components Used

| Component     | Value     | Package     | Notes                           |
|---------------|-----------|-------------|---------------------------------|
| R1, R2        | 10 kΩ     | 0805 SMD    | Equal values for filter base   |
| C1, C2, C4    | ~169 nF   | 0805 SMD    | Chosen for 100 Hz cutoff       |
| OPA277UA      | Precision Op-Amp | SOIC-8  | Low offset and drift           |
| Switch (SPDT) | JS202011SCQN | SMD       | Manual toggle between modes    |
| Connector     | SMD header | 2-pin/3-pin | For signal I/O                 |

---

## 📌 Applications

- Analog signal preprocessing
- Audio filtering
- Instrumentation front-ends
- Educational demonstration of filter design

---

## 📷 Preview

![3D PCB View](Altium/3DView.png)

---

## 📜 License

MIT License – feel free to use, modify, and share.

---

## 🤝 Contribution

Have an idea or improvement? Feel free to open a PR or issue. For suggestions on component alternatives or layout optimization, contributions are welcome!



