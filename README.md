# 5G-Network-Behavior-Testing-UERANSIM-Open5GS
Hands-on experiments showing UE–gNB–Core behavior in a 5G network under different configurations, with detailed logs and packet captures.


---

## 📑 Logs & PCAPs
Each experiment includes:
- **UE logs** (registration, PDU setup, slice/APN behavior)  
- **gNB logs** (SCTP/NGAP handling)  
- **Core Network logs** (AMF, SMF, UDM authentication & session data)  
- **Wireshark traces** showing NGAP and NAS signaling  

---

## 🛠 Environment Setup
- **PC1** → UERANSIM (UE)  
- **PC2** → UERANSIM (gNB)  
- **PC3** → Open5GS (Core)  
- **Tools** → Wireshark, Ubuntu Linux  

---

## 🚀 How to Reproduce
1. Set up UERANSIM UE on **PC1**.  
2. Deploy UERANSIM gNB on **PC2**, connected to the Core.  
3. Run Open5GS Core Network on **PC3**.  
4. Use provided configs to replicate scenarios.  
5. Logs and pcaps will be generated automatically.  

---

## 📖 Future Work
- Perform deeper protocol decoding (NGAP/NAS).  
- Automate distributed test scenarios.  
- Extend experiments toward **6G-inspired features**.  

---

✨ Contributions, feedback, and discussions are welcome!
