# Cybersecurity Incident Report: Network Traffic Analysis


-------

# Description <a name="description">

I conducted a cybersecurity incident report for a fictional company providing IT consultant services. This assessment was completed as a component of my cybersecurity portfolio and as part of the <a href='https://www.coursera.org/google-certificates/cybersecurity-certificate'>Google Cybersecurity Professional Certificate</a> on Coursera, specifically in the  <a href='https://www.coursera.org/learn/networks-and-network-security'> "Connect and Protect: Networks and Network Security" </a> Course.


The goal of this project is to analyze DNS and ICMP traffic in transit using data from a network protocol analyzer tool. Knowing how to identify potentially malicious traffic on a network can help cybersecurity analysts assess security risks on a network and reinforce network security.


# Scenario  <a name="scenario">
You are a cybersecurity analyst working at a company that specializes in providing IT consultant services. Several customers contacted your company to report that they were not able to access the company website www.yummyrecipesforme.com, and saw the error “destination port unreachable” after waiting for the page to load. 

You are tasked with analyzing the situation and determining which network protocol was affected during this incident. To start, you visit the website and you also receive the error “destination port unreachable.” Next, you load your network analyzer tool, tcpdump, and load the webpage again. This time, you receive a lot of packets in your network analyzer. The analyzer shows that when you send UDP packets and receive an ICMP response returned to your host, the results contain an error message: “udp port 53 unreachable.” 

------------------------

<p align="center">
Data: <br/>
<img src="https://i.imgur.com/BuW3XCk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Now that you have captured data packets using a network analyzer tool, it is your job to identify which network protocol and service were impacted by this incident. Then, you will need to write a follow-up report. 

As an analyst, you can inspect network traffic and network data to determine what is causing network-related issues during cybersecurity incidents. 

This incident, in the meantime, is being handled by security engineers after you and other analysts have reported the issue to your direct supervisor. 
   
## Cybersecurity Incident Report Assessment  <a name="workflow">

Provide a summary of the problem found in the DNS and ICMP traffic log.

My Response: 

The UDP protocol's findings indicate that the DNS server is either offline or inaccessible. This is supported by the network analysis results, which showed that the ICMP echo reply produced an error message stating "udp port 53 unreachable." Port 53 is typically used for DNS protocol traffic, reinforcing the likelihood that the DNS server is unresponsive.

------------------------

Explain your analysis of the data and provide at least one cause of the Incident.

My Response:

Today, at 1:23 p.m., an incident occurred. Customers reached out to the organization, reporting that they encountered the message "destination port unreachable" while attempting to access the website. The organization's network security experts are presently looking into this matter in order to restore customer access to the website. 

During our investigation into the issue, we conducted packet sniffing tests utilizing tcpdump. In the resulting log file, we discovered that DNS port 53 was inaccessible. Our next step involves determining whether the DNS server is inactive or if traffic to port 53 is being obstructed by the firewall. The DNS server may be inactive as a result of a successful Denial of Service attack or a configuration error.
