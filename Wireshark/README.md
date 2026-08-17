# Wireshark DNS Analysis Lab

Performed DNS traffic analysis using Wireshark to identify normal and suspicious query behavior.

### DNS Results

- Interface: Wi‑Fi
- Filter: dns
- Normal Traffic: googleapis, cloudflare, microsoft
- Traffic Selected for Investigation: unusual domains, repeated queries, NXDOMAIN responses
- Goal: Differentiate legitimate DNS activity from abnormal patterns

### Tools

Wireshark

### Evidence

**Normal DNS Traffic**  
![Normal DNS Traffic](Images/01-dns-normal.png)

**Traffic Selected for Investigation**  
![Traffic Selected for Investigation](Images/02-dns-suspicious.png)
