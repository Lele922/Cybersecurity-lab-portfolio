# Nmap Scan - Metasploitable2

## Objective
Identify open ports and running services on target machine.

## Command Used
```bash
nmap -sV -sC 192.168.56.102
```
## Results

| Port | Service | Version     |
|------|--------|--------------|
| 21   | FTP    | vsftpd 2.3.4 |
| 22   | SSH    | OpenSSH      |
| 80   | HTTP   | Apache       |

## Analysis

The FTP service (vsftpd 2.3.4) is known to be vulnerable and could be exploited.

## Conclusion

The target exposes multiple services that may be used for further exploitation.
