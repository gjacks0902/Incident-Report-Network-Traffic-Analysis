<Strong>Cybersecuirty Incident Report: Network Traffic Analysis</strong>
<p>
  <img width="902" height="448" alt="image" src="https://github.com/user-attachments/assets/243e3b9e-9425-426d-8d96-b92bbdb06993" />
</p>

<p>
  <em>Part 1: Provide a summary of the problem found in the DNS and ICMP traffic log</em>
  
  According to the DNS protocol, when using the UDP protocol to contact the DNS server in order to retreieve the IP address for the domain name. Following UDP, the ICMP protocol was used in order to diagnose network communication issues within servers/routers. The error message in the logs shows "port 53 unreachable". Port 53 is a standard network protocol normally used in DNS service. Which is what translates the domain name into IP addresses. The DNS ID of 35084 with the plus sign indicates a flag/responsive query. And the A? is the client requesting an IPv4 address. Given this information, it's highly likely because when the DNS server is trying to find the message request from UDP. Which would suggest a non responsive DNS server.
</p>
<br>
<p>
  <em>Part 2: Explain your analysis of the data and provide at least one cause of the incident.</em>

  This incident occurred at 1:24pm. Many of the customers had reported the fact that whenever they tried to reach the website, they'd see an error message reporting "destination port unreachable". Once the security team was notified, we immediately started to work on investigation using the network analyzer tool, tcpdump. The logs revealed that port 53 was unreachable. The next step is to figure out if this server is down or the firewall is blocking port 53. The team believes that this could most likely be caused by a successful DDoS attack.
</p>
