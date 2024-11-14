# DESCRIPTION
This repository contains Proofs of Concept (PoCs) for known Server-Side Request Forgery (SSRF) vulnerabilities in ArcGIS, a powerful geographic information system (GIS) software used for mapping and spatial analysis. Each PoC demonstrates specific exploitation techniques to enhance awareness of security risks associated with these vulnerabilities. The content is intended for educational and research purposes only.

It is important to note that this endpoints should only be considered vulnerable if they are exposed to unauthenticated users, as they contain dangerous functionality meant for authenticated users. 

I discovered this SSRF while working as an SRT in Synack.

# METHODOLOGY USED
First discover which ArcGIS services are exposed by the target, then review the documentation of each of them(you may be able to find more than an SSRF).

# DISCLAIMER
The content provided in this repository is for educational and research purposes only. The Proofs of Concept (PoCs) related to Server-Side Request Forgery (SSRF) vulnerabilities in ArcGIS are intended to demonstrate security weaknesses and should not be used for malicious activities or unauthorized access to any system.

By using this repository, you agree to conduct your activities in accordance with all applicable laws and regulations. The authors and contributors do not assume any liability for damages resulting from the misuse of the information contained herein. Always obtain proper authorization before testing security vulnerabilities on any system.

Use responsibly and ethically.
