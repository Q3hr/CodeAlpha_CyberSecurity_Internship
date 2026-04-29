# 🔐 CodeAlpha Cyber Security Internship Projects

> Practical cybersecurity projects completed during the **CodeAlpha Cyber Security Internship Program**, covering network analysis, phishing awareness, and secure coding.

---

## 👨‍💻 Intern Details

| Field | Details |
|---|---|
| **Name** | Ibrar Ul Hassan Shami |
| **Student ID** |  CA/DF1/41003 |
| **Program** | Cyber Security |
| **Internship** | CodeAlpha Cyber Security Internship |

---

## 📂 Repository Contents

| Task | Description |
|---|---|
| Task 1 | Basic Network Packet Sniffer |
| Task 2 | Phishing Awareness Training |
| Task 3 | Secure Coding Review |

---

## 📡 Task 1 — Basic Network Sniffer

A Python-based network sniffer built using the **Scapy** library that captures and analyzes network packets.

### Features
- Captures live network packets
- Displays Source & Destination IP
- Shows protocol information
- Helps understand real network traffic

### Code

```python
from scapy.all import sniff, IP

def packet_callback(packet):
    if packet.haslayer(IP):
        print("Source:", packet[IP].src)
        print("Destination:", packet[IP].dst)
        print("Protocol:", packet[IP].proto)

sniff(prn=packet_callback, count=10)
```

### Learning Outcomes
- Understanding packet sniffing
- Network traffic analysis
- Basic protocol inspection

---

## 🎣 Task 2 — Phishing Awareness Training

Educational task focused on phishing attacks and social engineering techniques.

### Topics Covered
- What is phishing
- Common phishing techniques
- Fake email & login page examples
- Prevention methods

### Prevention Tips
- ✅ Verify sender email addresses
- ✅ Do not click suspicious links
- ✅ Enable two-factor authentication
- ✅ Check website URLs carefully

---

## 🔒 Task 3 — Secure Coding Review

Security review of a login system — identifying vulnerabilities and applying secure coding practices.

### ❌ Vulnerable Code

```python
username = input("Enter Username: ")
password = input("Enter Password: ")

if username == "admin" and password == "1234":
    print("Login Successful")
else:
    print("Access Denied")
```

### Vulnerabilities Found
- Hardcoded credentials
- Plaintext password storage
- No encryption
- No brute-force protection

### ✅ Secure Implementation

```python
import hashlib

stored_password = hashlib.sha256("1234".encode()).hexdigest()

username = input("Enter Username: ")
password = input("Enter Password: ")

entered_password = hashlib.sha256(password.encode()).hexdigest()

if username == "admin" and entered_password == stored_password:
    print("Login Successful")
else:
    print("Access Denied")
```

### Security Improvements
- Password hashing with SHA-256
- Secure credential comparison
- Improved authentication security

---

## 🛠 Technologies Used

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Scapy](https://img.shields.io/badge/Scapy-Network_Analysis-blue?style=flat)
![Security](https://img.shields.io/badge/Cybersecurity-Internship-red?style=flat)

- Python 3.x
- Scapy
- Hashlib
- Cybersecurity principles
- Network analysis

---

## 🚀 How to Run

### Clone Repository
```bash
git clone https://github.com/MAK554267/CodeAlpha_CyberSecurity_Internship.git
cd CodeAlpha_CyberSecurity_Internship
```

### Run Network Sniffer
```bash
python Task1_NetworkSniffer/network_sniffer.py
```

### Run Secure Login Program
```bash
python Task3_SecureCodingReview/secure_login.py
```

> ⚠️ **Note:** The network sniffer requires Administrator/root privileges to capture raw packets.

---

## 📚 Learning Outcomes

Through this internship I learned:
- ✔ Network packet analysis
- ✔ Social engineering awareness
- ✔ Secure coding techniques
- ✔ Vulnerability identification
- ✔ Basic cybersecurity practices

---


<p align="center">Made with 💻 during CodeAlpha Cyber Security Internship</p>
