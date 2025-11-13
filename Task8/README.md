\# Task 8 — Network Traffic Capture with Wireshark



\## Objective

Capture and analyze HTTP network traffic using Wireshark.



\## Steps

1\. Opened Wireshark on Kali Linux.

2\. Selected interface `eth0` for capturing live packets.

3\. Visited HTTP websites such as example.com and neverssl.com.

4\. Applied filter `http` to view only HTTP packets.

5\. Observed HTTP GET and response packets, URLs, hostnames, and IP information.

6\. Saved the capture as `wireshark\_capture.pcap`.



\## Key Observations

\- HTTP packets are unencrypted.

\- GET requests show full URL and hostname.

\- Response packets contain headers like status code (200 OK).

\- Source and destination IP/ports are visible.



\## Deliverables

\- `wireshark\_capture.pcap`

\- `README.md`



