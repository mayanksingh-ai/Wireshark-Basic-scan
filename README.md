# Wireshark-Basic-scan
Task 5 elevate labs
# 📡 Wireshark Network Traffic Analysis

## 🎯 Objective
Capture and analyze network traffic using Wireshark, apply protocol filters, identify different protocols, and export the capture as a `.pcap` file.

---

## ✅ Prerequisites
- Wireshark installed: https://www.wireshark.org/download.html

---

## 🖥️ Step 1: Install Wireshark
1. Download Wireshark from https://www.wireshark.org/download.html  
2. Run the installer and follow default installation steps.  
3. Launch Wireshark after installation.  

---

## 🖥️ Step 2: Start Capturing on Active Interface
- Open **Wireshark**.  
- From the start screen, select your **active network interface** (e.g., Wi-Fi, Ethernet).  
- Click the **blue shark fin** (Start Capturing).  

---

## 🖥️ Step 3: Generate Network Traffic
- Open a web browser and visit https://example.com
- 
---

## 🖥️ Step 4: Stop Capture
- Let the capture run for about **1 minute**.  
- Click the **red square** (Stop Capturing).  

---

## 🖥️ Step 5: Filter Captured Packets by Protocol
Use the **Display Filter** bar at the top of Wireshark:

**HTTP**

- http
  
**DNS**

- dns
  
**TCP**

- tcp

  
(You can combine filters, e.g., `tcp && !dns`)  

---

## 🖥️ Step 6: Identify at Least 3 Protocols
Confirm at least three different protocols in your capture. Common examples:
- **DNS** – Domain name lookups (queries/responses)  
- **TCP** – Reliable transport (3-way handshake, segmentation, ACKs)  
- **HTTP/HTTPS** – Web requests/responses  
- *(You may also see ARP, ICMP, TLS, QUIC, etc.)*  

---

## 🖥️ Step 7: Export the Capture as `.pcap`
- Go to **File → Save As…**  
- Choose a location and name, e.g., `network_capture.pcap`  
- **Save as type:** `pcapng` (default) or select `pcap` if required by your tools.  

---

## 🖥️ Step 8: Summarize Findings

### ✅ Observations
- Captured at least **3 protocols**: DNS, TCP, HTTP.  
- **DNS** resolved domain names to IP addresses (e.g., `example.com → 93.184.216.34`).  
- **TCP** connections showed the **3-way handshake** (SYN → SYN/ACK → ACK).  
- **HTTP** traffic included **GET** requests and **200 OK** responses.  

### 🔍 Example Packet Details
- **DNS Query**  
  - Query Name: `example.com`  
  - Response: A record with IP `93.184.216.34`  

- **TCP Handshake**  
  - Client → Server: SYN  
  - Server → Client: SYN/ACK  
  - Client → Server: ACK  

- **HTTP Request/Response**  
  - Request: `GET /index.html HTTP/1.1`  
  - Response: `HTTP/1.1 200 OK`  

### 📊 Summary Table
| Protocol | Example Frame No. | Purpose                  | Notes                          |
|----------|-------------------|--------------------------|--------------------------------|
| DNS      | 12                | Name resolution          | Query `example.com` → A record |
| TCP      | 25–27             | Connection establishment | SYN, SYN/ACK, ACK              |
| HTTP     | 40                | Web request/response     | `GET /index.html` → `200 OK`   |

---

## 📝 Conclusion
Wireshark successfully captured live traffic. Using filters (`http`, `dns`, `tcp`) made analysis easier. The capture demonstrates DNS lookups, TCP handshakes, and HTTP communication. Exporting to `.pcap/.pcapng` allows further offline analysis.


