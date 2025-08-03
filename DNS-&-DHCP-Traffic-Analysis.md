# DNS Tunneling Analysis

**Capture Name:** dns_tunneling_traffic.pcapng  
**Date:** August 3, 2025  
**Tool Used:** Wireshark  
**Tunneling Tool:** iodine

## Summary
This capture simulates DNS tunneling using `iodine`. Traffic shows abnormally long DNS queries to `tunnel.testdomain`.

## Indicators
- Domain Queried: `tunnel.testdomain`
- Encoded subdomain patterns in queries
- Repeated use of `TXT` record types
- Regular beaconing pattern

## Wireshark Filters Used 
- Router = 192.168.12.1: This is the host network ID/DCHP server

## Full Demo

- Step 1. Open Wireshark via Terminal
<img width="941" height="977" alt="Step1" src="https://github.com/user-attachments/assets/35105493-beaf-4658-b1a4-8d76fa3601af" />

 

- Step 2. Select NIC
<img width="1920" height="1080" alt="step2" src="https://github.com/user-attachments/assets/f79dc64c-ce97-4cf9-a6b3-1c5671e5f551" />
<img width="1920" height="1080" alt="Step 2 1" src="https://github.com/user-attachments/assets/d9b6b6e3-6800-4914-9743-b1fd11792b9a" />


- Step 3. Filter to  DNS/DHCP
<img width="947" height="1071" alt="Step 3" src="https://github.com/user-attachments/assets/6a794511-8ce8-44e4-b58e-71e9c6ed8e06" />


- Step 4. Allow DNS traffic capture
<img width="894" height="979" alt="Step4" src="https://github.com/user-attachments/assets/a8c395c7-4792-4099-991e-4f43e054a458" />


- Step 5. Use iodine to simmulate DNS tunneling to 'tunnel.testdomain'.
<img width="951" height="917" alt="step5" src="https://github.com/user-attachments/assets/5fa36b1e-a90d-4a26-b69d-a9bfa7bc21bf" />
<img width="1920" height="1080" alt="step5 1" src="https://github.com/user-attachments/assets/0b772f24-42bb-4634-ac74-ee6913bff92d" />


## DNS Tunneling Detection

Captured a simulation of DNS tunneling using `iodine` on Kali Linux. Used Wireshark to identify suspicious patterns such as long DNS queries, base64 payloads, and TXT record abuse.

**Skills Highlighted:**
- DNS protocol analysis
- Use of open-source tools (iodine, Wireshark)
- Network traffic investigation
