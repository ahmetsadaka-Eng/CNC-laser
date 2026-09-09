# ⚡ CNC Laser PCB Masking & Etching Machine

An automated, low-noise, and rapid prototyping 2-axis CNC laser system designed for in-house Printed Circuit Board (PCB) fabrication.

---

## 📌 Project Overview

Traditional desktop PCB prototyping usually relies on CNC mechanical milling, which suffers from heavy tool wear, high acoustic noise, airborne fiberglass dust, and fragile micro-endmills breaking. 

This graduation project introduces a photochemical-assisted direct laser masking approach:
1. **Base Coating:** A uniform layer of black resist (ink/paint) is applied to the copper-clad laminate.
2. **Laser Ablation / Exposure:** The CNC laser precisely ablates the negative mask along the trace boundaries according to the circuit layout.
3. **Chemical Etching:** The board is immersed in **Ferric Chloride ($FeCl_3$)**, dissolving all exposed copper areas while preserving the masked circuit traces.
4. **Resist Stripping:** The remaining ink layer is cleaned off, leaving a clean, high-precision copper circuit board ready for drilling and soldering.

---

## ✨ Key Advantages

* 🔇 **Silent Operation:** Eliminates high-RPM spindle noise typical of mechanical isolation routing.
* ⏱️ **Fast & Repeatable:** Streamlined workflow from Gerber/G-code directly to chemical bath.
* 🛠️ **Zero Tool Wear:** Non-contact optical processing means no broken engraving bits or tool offset recalibrations.
* 🧼 **Clean & Safe:** Generates no hazardous fiberglass (FR4) dust compared to dry CNC milling.

---

## ⚙️ Technical Specifications & Hardware

| Subsystem | Component / Specification |
| :--- | :--- |
| **Microcontroller** | STM32 ARM Cortex-M (32-bit real-time motion control) |
| **Actuators** | High-torque NEMA Stepper Motors |
| **Optical Module** | Focused Diode Laser Module |
| **Structural Frame** | Modular Aluminum V-Slot / T-Slot (Sigma Profiles) |
| **Etchant Used** | Ferric Chloride ($FeCl_3$) Solution |

---

## 🚀 Workflow Pipeline

```text
[PCB CAD Design] ➔ [Gerber / G-code Generation] ➔ [Ink Spray Coating]
                             ↓
              [STM32 CNC Laser Contouring]
                             ↓
               [Ferric Chloride Bath (Etch)]
                             ↓
                  [Ink Removal & Clean] ➔ [Ready PCB]
