# 🧪 Day 17: Network Troubleshooting & Diagnostics

On Day 17 of my Linux journey, I focused on exploring **network troubleshooting tools** essential for diagnosing issues related to connectivity, DNS, and routing. I practiced tools like `netstat`, `ss`, `traceroute`, `dig`, and `curl` and learned how to detect potential failures or delays.

---

## 📌 Key Takeaway

> I learned that when you try to visit a website like Google, your machine sends packets that travel through multiple **routers (hops)** to reach the destination server.  
> Using `traceroute`, I was able to visualize and understand this process.

---

## 🧰 Tools Practiced

### 1️⃣ Installed Basic Network Tools
Installed tools required for diagnostics including `net-tools`, `iputils-tracepath`, and `dnsutils`.

---

### 2️⃣ Checked Active Network Connections

netstat -tuln
Lists all listening TCP/UDP ports with numerical IPs and ports.

3️⃣ Checked Routing Table

netstat -r
Displays system routing table including default gateway.

4️⃣ & 5️⃣ Used ss for Socket Statistics

ss -tuln      # View open sockets
ss -tan       # Detailed TCP connection info
ss -l         # List all listening ports
ss provides more detailed and faster output than netstat.

6️⃣ Traced Packet Path with traceroute

traceroute www.google.com
Visualized each hop taken to reach Google's server.

Learned that some routers drop ICMP replies (represented as * * *).

Also tried with ICMP:

traceroute -I www.google.com
And via TCP:

traceroute -T -p 80 www.google.com

7️⃣ Queried DNS Info with dig

dig www.google.com
Retrieved A records (IP addresses) for Google.

Queried specific records:

dig www.google.com MX
Noted that MX records are associated with the domain root (not subdomains).

8️⃣ Tested Web Connectivity with curl

Checked website status codes:
curl -I https://whatismyipaddress.com/

This could not resolve host, indicating that the server was probably blocking it.

Also tested my website, the DNS resolution succeeded but the server didn't respond because the server is down.

📷 Screenshots in image folder
1. Installed network tools
2. Checked active network connections
3. Checked routing table
4. Used ss -tuln to view more detailed network information
5. Viewed detailed connection info with ss -tan
6. Checked listening ports with ss -l
7. Ran traceroute to view the path that packets take to reach destination from my machine
8. Checked with traceroute -i and noticed some routers didnt respond to ICMP
9. Traced using TCP packets
10. Queried Google IPs with dig
11. Checked MX records
12. Used curl to check status code of a website
13. also checked the status code of my website

✅ What I Learned
- How to trace network routes with traceroute

- The difference between UDP, ICMP, and TCP probes in traceroute

- How to use dig for A and MX DNS record queries

- How to verify if a domain is online or unreachable using curl

- That network requests can fail even after DNS succeeds (e.g., server timeout)
