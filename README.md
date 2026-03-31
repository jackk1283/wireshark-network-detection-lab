# wireshark-network-detection-lab

Analyzed network traffic in Wireshark to identify suspicious behavior. Established a normal baseline, then detected a host performing port scanning and service discovery across multiple ports. Further analysis showed SMB authentication attempts and sustained internal communication, indicating possible lateral movement. Used TLS metadata (SNI) to rule out legitimate encrypted traffic. No command-and-control beaconing was observed.
