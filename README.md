# 📡 5G Network Behavior Testing using UERANSIM & Open5GS

---

## Acknowledgement
This project was carried out as part of my academic and research journey in 5G networks.  
I would like to acknowledge the open-source developers and contributors of **Open5GS** and **UERANSIM**, whose efforts made it possible to implement and test a complete 5G setup in a lab environment.  

---

## 📑 Abstract
The transition from 4G to 5G introduces several enhancements such as **network slicing, improved authentication, QoS differentiation, and new service capabilities**.  
This project focuses on understanding **how a 5G network reacts to different UE and Core configuration changes** by simulating various scenarios using **UERANSIM** (UE and gNB) and **Open5GS** (Core Network).  

Experiments included **IMSI modifications, duplicate UE sessions, slice and APN changes, OPC variations, and initial PDU session slice changes**. Logs and Wireshark captures were collected for each scenario to analyze **protocol-level behavior, registration outcomes, and authentication responses**.  

---

## 📖 Introduction
Fifth Generation (5G) wireless systems provide enhanced connectivity, enabling features like **eMBB, URLLC, and mMTC**. However, the flexibility of 5G also raises challenges for testing how the network **responds to unusual or dynamic UE behavior**.  

In this project, a **distributed 5G testbed** was set up with three components:  
- **PC1 → UE (UERANSIM)**  
- **PC2 → gNB (UERANSIM)**  
- **PC3 → Core Network (Open5GS)**  

This environment allowed for controlled experiments to analyze **authentication, session establishment, and network slicing behavior**.

---

## 🎯 Project Scope
- Deploy a 5G Core and RAN simulation across multiple machines.  
- Run baseline and modified UE registration scenarios.  
- Observe **authentication failures, slice selection impacts, and duplicate UE handling**.  
- Collect and analyze logs and Wireshark packet captures.  
- Provide structured data and observations for students, researchers, and practitioners.  

---

## 🔑 Definitions
- **IMSI (International Mobile Subscriber Identity):** Unique identifier for subscribers.  
- **S-NSSAI (Single Network Slice Selection Assistance Information):** Identifies slices allocated to UEs.  
- **APN (Access Point Name):** Defines the gateway for packet data networks.  
- **OPC (Operator Code):** Parameter in Milenage algorithm for UE authentication.  
- **PDU Session:** Logical data session established between UE and the Core for internet connectivity.  

---

## 🏗 System Design
The project was built on a **three-PC distributed architecture**:

- **PC1: UE (UERANSIM)**  
  Simulated User Equipment generating traffic and performing registrations.  

- **PC2: gNB (UERANSIM)**  
  Served as the access node, forwarding UE traffic to the Core.  

- **PC3: Core Network (Open5GS)**  
  Provided full 5G Core Network functions (AMF, SMF, UPF, UDM, AUSF).  

Additional tools:  
- **Wireshark** for NGAP and NAS protocol analysis.  
- **Linux SCTP support** for UE–gNB communication.  

---

## ⚙️ Implementation
The following steps were carried out to build the setup:  
1. Install and configure **Open5GS** on PC3.  
2. Deploy **UERANSIM UE** on PC1 and **UERANSIM gNB** on PC2.  
3. Configure the UE and gNB with IMSI, slice, APN, and OPC values.  
4. Connect the gNB to the Core Network via NGAP over SCTP.  
5. Run multiple scenarios by modifying UE parameters.  
6. Capture logs (UE, gNB, Core) and Wireshark traces.  

---

## 🧪 Experiments Conducted
1. **Normal Connection** – Baseline registration and session establishment.  
2. **IMSI Change** – Observing network behavior with modified IMSIs.  
3. **Duplicate UEs** – Running UEs simultaneously and sequentially.  
4. **Slice (S-NSSAI) Change** – Testing slice selection flexibility.  
5. **APN Change** – Impact of modifying APN values on session setup.  
6. **Initial PDU Slice Change** – Session behavior when PDU slice changes at start.  
7. **OPC Change** – Authentication failures with modified OPC.  

---

