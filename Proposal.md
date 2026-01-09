📄 AMPRNet Project Proposal
1. Applicant Information
Callsign: VU33JD
Name: Jay Gurubalan
Location: Pondicherry, India
2. Project Title
Experimental APRS and Ham Data Transport over Radio-Based IP Links
3. Abstract
This project proposes to build and study an experimental amateur radio IP network using Raspberry Pi computers and radio links to transport APRS packets and other ham data between isolated radio regions without using the public internet. The project will investigate reliability, latency, packet loss, and routing behavior of IP networks operating entirely over amateur radio links.
4. Background and Motivation
Currently, most APRS and ham data traffic depends heavily on the public internet (APRS-IS, DMR networks, etc). In disaster scenarios or in remote areas, this dependency may not be available. Amateur radio has a long tradition of experimenting with independent communication networks.
This project aims to explore how APRS and small data services can be carried over a ham-only IP network and to study the practical behavior of such networks under real radio link conditions.
5. Objectives
Build a ham-only IP network using radio links
Transport APRS and ham data between isolated radio areas without using the public internet
Study:
Link reliability
Latency
Packet loss
Routing stability
Experiment with store-and-forward techniques during link outages
6. Technical Description
6.1 Network Concept
Instead of using the public internet:
Radio → Internet → APRS Servers
The project uses:
Radio → Raspberry Pi → IP over Radio → Raspberry Pi → Radio
Each site will contain:
A Raspberry Pi
A radio or RF data link
APRS software (Direwolf, aprx, or equivalent)
Linux-based routing
The IP connectivity between sites will be carried exclusively over amateur radio links (e.g., Wi-Fi point-to-point links, mesh nodes, or other RF data links).
6.2 Architecture (Initial Phase)
[Site A]                         [Site B]
Radio + Raspberry Pi  ← RF IP →  Raspberry Pi + Radio
 Local APRS                        Local APRS
Additional sites may be added later to form a small experimental network or mesh.
7. Use of 44Net Address Space
The 44Net address space will be used for:
Addressing experimental nodes
Routing IP traffic between radio-linked sites
Testing ham-only IP services and routing behavior
No commercial hosting, public web services, or general-purpose internet services will be operated.
8. Equipment
Raspberry Pi computers
VHF/UHF radios and/or Wi-Fi radio links
Antennas
Linux networking software
APRS software (Direwolf, aprx, etc.)
9. Regulatory Compliance
All transmissions will comply with amateur radio regulations
No encrypted user traffic
No commercial or third-party traffic
Network will be used strictly for experimentation and research
10. Expected Results
A working prototype ham-only IP network
Measured performance data (latency, loss, stability)
Practical experience with IP routing over RF
A platform for future emergency and experimental communications research
11. Project Scope
This is an experimental and research network, not a production service and not a replacement for APRS-IS or the public internet.
12. Summary
This project will explore the practical use of IP networking over amateur radio links by transporting APRS and ham data without reliance on the public internet, in line with the experimental goals of the AMPRNet.
