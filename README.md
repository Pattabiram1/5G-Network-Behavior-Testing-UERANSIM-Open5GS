# 📡 5G Network Experiments using UERANSIM & Open5GS (Multi-PC Setup)

## 📌 Project Overview
This repository documents my experiments with a **distributed 5G setup** using **UERANSIM** and **Open5GS**.  
To emulate a realistic deployment, I distributed the components across three machines:

- **PC1** → UE (UERANSIM)  
- **PC2** → gNB (UERANSIM)  
- **PC3** → 5G Core Network (Open5GS)  

This setup allowed me to study **end-to-end 5G procedures** such as registration, authentication, session management, and slicing by modifying configurations and observing the resulting behavior.

---

## 🎯 Experiments Performed
- ✅ Normal UE–gNB–Core connection  
- 🔄 Changing **IMSI** values (subscriber identity testing)  
- 📱 Running **duplicate UEs** (simultaneous and sequential)  
- 🛰️ **Network slice (S-NSSAI) changes** at UE  
- 🌐 **APN modifications** (different data networks)  
- 📶 **Initial PDU session slice changes**  
- 🔑 **OPC (Operator Code) variations** for authentication  

---


