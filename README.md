# CS-305-11908-M01-Software-Security-2025

## About  
This repository is part of my ongoing CS portfolio. It showcases my work in software security and vulnerability assessment. Included are completed project artifacts and reflections demonstrating my ability to identify risks, improve code security, and apply tools to verify safe software practices.

## Repository Contents

### Project 1 – Artemis Financial Vulnerability Assessment Report  
**Summary (What problem did it solve?):**  
This project involved analyzing Artemis Financial’s RESTful API for outdated or vulnerable dependencies. The company wanted to uncover third-party risks that could impact their operations. I performed static analysis using the OWASP Dependency-Check Maven plug-in and summarized the findings in a professional security report.  

**What I did particularly well:**  
I configured the dependency-check tool to produce a clear and readable report and suppressed false positives through a custom suppression file. I also documented risks in a way nontechnical stakeholders could understand.

**Where could I enhance my code, and how would it help?:**  
I could include additional layers like automatic alerts for newly discovered CVEs or integrate the tool with a CI/CD pipeline to catch vulnerabilities earlier. This would make the system more proactive and scalable.

**Which pieces were most challenging, and how did I overcome them?:**  
Fine-tuning the suppression logic and troubleshooting Maven plugin configurations was tough. I got through it by looking at OWASP documentation and experimenting with working test builds until the output was clean.

**Tools and resources added to my network:**  
- OWASP Dependency-Check  
- Maven suppression configuration  
- GitHub security workflow patterns  

**Skills transferable to other projects:**  
- Vulnerability scanning  
- Interpreting CVSS scores  
- Communicating risk to nontechnical audiences  

**How I made this project maintainable, readable, and adaptable:**  
I kept suppression and reports versioned in the repository and wrote the report in plain language with organized sections for easier updates.

---

### Project 2 – Artemis Financial Practices for Secure Software Report  
**Summary (What problem did it solve?):**  
This project focused on hardening Artemis Financial’s existing code by enabling HTTPS, refactoring for secure communication, and implementing a checksum endpoint. I added a self-signed certificate, hash verification using SHA-256, and made sure the application followed Spring Boot SSL configuration best practices.

**What I did particularly well:**  
I refactored the code cleanly to support HTTPS and checksum verification, then validated the output in a browser with a secure connection. The `/hash` endpoint demonstrated real-time hashing of custom strings with checksum confirmation.

**Where could I enhance my code, and how would it help?:**  
Using a CA-signed certificate and enforcing HTTP Strict Transport Security (HSTS) headers would move the project closer to real-world deployment standards.

**Which pieces were most challenging, and how did I overcome them?:**  
Creating the keystore and making sure it worked properly in Spring Boot required reading a lot of documentation and retrying config setups until the browser displayed the secure connection successfully.

**Tools and resources added to my network:**  
- Java Keytool  
- Spring Boot HTTPS docs  
- `MessageDigest` for SHA-256 hashing  

**Skills transferable to other projects:**  
- SSL certificate setup  
- Secure API refactoring  
- Writing and testing cryptographic functionality  

**How I made this project maintainable, readable, and adaptable:**  
Used config files for all sensitive data, modularized the hashing utility, and added screenshot verification for checksum validation and HTTPS functionality.

---

## Additional Reflections  

### How can I ensure that my code, program, or software is functional and secure?  
By testing changes incrementally, validating configuration settings, and verifying behavior through browser and tool-based feedback like dependency-check output and live endpoint tests.

### How do I approach software security?  
I start by identifying weaknesses (like outdated libraries or plain HTTP), then layer in protections like SSL, input validation, and hashing, and finally verify that changes didn’t introduce new risks.

### What tools or practices will I use again?  
OWASP Dependency-Check, MessageDigest, HTTPS configuration in Spring Boot, and Maven suppression workflows—all helped me improve security posture without breaking functionality.

---

## Collaborators  
For this assignment, I have added my instructor [**bretonne**](https://github.com/bretonne) as a collaborator so they can review my portfolio work.

## Acknowledgments  
Thanks to my instructor, my classmates, and Southern New Hampshire University (SNHU) for their support, insights, and guidance throughout the CS-305 course.

## Contact  
For any questions or suggestions, feel free to open an issue or contact me directly.
