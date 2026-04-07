# Three-Phase Linear Induction Motor

> **EEE-206 — Energy Conversion Laboratory | Section B2, Group 5**  
> Department of Electrical and Electronic Engineering  
> Bangladesh University of Engineering and Technology (BUET)

---

## 📋 Project Overview

This project involves the **design, construction, and testing of a single-sided three-phase Linear Induction Motor (LIM)**. Unlike conventional rotary induction motors, a LIM produces linear thrust instead of rotational torque — achieved by conceptually "unrolling" a rotary motor into a flat, linear form.

The motor was built and tested under both **2-pole** and **4-pole** configurations to compare speed and torque characteristics.

---

## Team Members

| Name | Student ID |
|------|------------|
| Anik Biswas | 1906125 |
| Monir Hossain | 1906126 |
| Nafisa Nairun | 1906127 |
| Shahriyer Hasan | 1906128 |
| Al Fattah Siddique | 1906129 |
| Md. Mustansir Billah | 1906130 |
| Imtiaj Ahmed Fahim | 1606083 |

**Date of Submission:** 4 September 2022

---

##  Repository Contents

```
📦 linear-induction-motor
 ┣ 📄 README.md
 ┣ 📄 LinearInductionMotor_Report.pdf     ← Final formatted report (PDF)
 ┗ 📄 LinearInductionMotor_Report.docx    ← Editable Word document
```

---

## ⚙️ Motor Specifications

| Parameter | Value |
|-----------|-------|
| Type | Single-Sided Linear Induction Motor (SLIM) |
| Phases | 3 |
| Core | Laminated E-shaped iron cores (×60) |
| Winding Wire | 23-gauge copper wire |
| Turns per Coil | 80 |
| Winding Config | Double-layer |
| Rotor Material | Aluminium sheet |
| Pole Configurations Tested | 2-pole, 4-pole |

---

## 🔬 Key Concepts

**Linear Synchronous Speed:**
```
Vs = 2τf   (m/s)
```
where `τ` = pole pitch (m) and `f` = supply frequency (Hz)

**Slip:**
```
s = (Vs − v) / Vs
```

Speed and torque are controlled via the **consequent pole-changing method** — doubling the poles halves the speed and doubles the torque.

---

## 🚀 Applications

- Industrial automation (pick-and-place, robotics)
- CNC machine tool drives
- Maglev train propulsion
- Baggage handling systems
- Sliding doors and curtain openers
- Textile loom shuttle drives

---

##  Limitations Observed

1. **Air gap control** — difficulty maintaining a small, uniform air gap reduced induced flux
2. **Insufficient coil count** — stator coils were too few to induce adequate rotor voltage
3. **Poor insulation** — led to higher core and copper losses
4. **High slip** — inherent to LIM design, causing elevated secondary losses and lower efficiency

---

##  License

This project report is submitted for academic purposes at BUET. All rights reserved by the authors.
