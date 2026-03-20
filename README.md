# Metro DWDM Ring Network Design — 4-Node ROADM Architecture

## 📌 Overview

This project demonstrates the design of a metro-scale DWDM (Dense Wavelength Division Multiplexing) optical transport network using a 4-node ROADM-based ring topology.

The network connects major cities:

* Mumbai
* Pune
* Hyderabad
* Nagpur

The design focuses on optical transport engineering principles including span loss calculation, EDFA placement, and wavelength channel planning.

---

## 🖼️ Network Topology

![DWDM Network Diagram](./DWDM PROJECT DIAGRAM.drawio.png)

* Ring topology with ROADM nodes at each city
* Single-mode fibre (G.652D)
* Inline EDFAs placed based on span loss and distance

---

## ⚙️ Network Architecture

### 🔹 ROADM Nodes

Each node consists of:

* ROADM (Reconfigurable Optical Add-Drop Multiplexer)
* OTN Transponders (10G/100G client signal conversion)

ROADM enables:

* Add/drop wavelengths
* Pass-through traffic without O-E-O conversion

---

## 📡 Optical Parameters

| Parameter      | Value               |
| -------------- | ------------------- |
| Fibre Type     | G.652D Single Mode  |
| Attenuation    | 0.2 dB/km @ 1550 nm |
| Connector Loss | 0.5 dB              |
| Splice Loss    | 0.1 dB              |
| Safety Margin  | 3 dB                |

---

## 📉 Span Loss Calculation

### Formula:

Total Span Loss =
(Distance × Fibre attenuation) +
(Splices × splice loss) +
(Connectors × connector loss) +
Margin

---

## 📊 Link Budget Analysis

| Link               | Distance | Total Loss | EDFAs Required |
| ------------------ | -------- | ---------- | -------------- |
| Mumbai → Pune      | 150 km   | 37.75 dB   | 1              |
| Pune → Hyderabad   | 560 km   | 130 dB     | 6              |
| Hyderabad → Nagpur | 500 km   | 116.5 dB   | 5              |
| Nagpur → Mumbai    | 830 km   | 190.75 dB  | 9              |

---

## 🔁 EDFA Placement Strategy

* Amplifier placed approximately every **~80 km**
* Based on span loss threshold (~20 dB)
* Ensures signal integrity over long-haul fibre links

---

## 🌈 DWDM Channel Plan

* Band: C-band (1530–1565 nm)
* Channel spacing: 100 GHz (ITU-T G.694.1)
* Total channels: 40

### Capacity:

* Each channel: 100G (OTU4)
* Total ring capacity: **4 Tbps**

---

## 📡 Channel Allocation

| Channel Range | Route                           |
| ------------- | ------------------------------- |
| Ch 1–2        | Mumbai ↔ Pune                   |
| Ch 3–8        | Pune ↔ Hyderabad                |
| Ch 9–16       | Hyderabad ↔ Nagpur              |
| Ch 17–28      | Nagpur ↔ Mumbai                 |
| Ch 29–40      | Ring protection / express paths |

---

## 🧠 Key Learnings

* Optical span loss budgeting and link engineering
* EDFA placement for long-haul DWDM systems
* ROADM-based dynamic wavelength switching
* High-capacity optical transport design (Tbps scale)
* Real-world telecom network planning concepts

---

## 🎯 Use Case

This design simulates a **carrier-grade metro optical transport network** used by ISPs and hyperscalers for backbone connectivity.

---

## 🛠️ Tools Used

* Draw.io (Network Diagram)
* Optical network planning concepts (manual calculations)

---

## 👨‍💻 Author

Mustafa Indorewala
Network Engineer | Optical & Data Centre Enthusiast

