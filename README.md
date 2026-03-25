# wireshark-network-detection-lab

This lab analyzes network traffic using Wireshark to distinguish normal behavior from suspicious activity. A baseline capture of a home network showed typical modern traffic patterns dominated by TLS and QUIC with no signs of beaconing or abnormal protocol usage.

Analysis of a separate PCAP revealed a single internal host performing reconnaissance and service discovery by initiating connections across multiple enterprise ports (SMB, LDAP, RPC, HTTP/HTTPS), followed by repeated SMB probing and SYN-based scanning behavior. Further inspection identified SMB2 session setup and NTLM authentication attempts with IPC$ access, consistent with internal enumeration and early lateral movement activity.

Additional analysis of TLS traffic demonstrated how encrypted sessions can still be investigated using metadata such as Server Name Indication (SNI) and JA3 fingerprinting, enabling visibility into destination domains and client behavior without decrypting payloads.

No evidence of command-and-control beaconing was observed in the analyzed traffic.
