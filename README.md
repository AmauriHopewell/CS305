This is a project summarizing security-improvement work I did for a web server app for a client named Artemis Financial.
Artemis Financial is a financial consulting firm for which security is very important, because it develops individualized financial plans for savings, retirement, investments, and insurance,
so it commonly handles sensitive client data like SSNs and tax information. 
The company needed a secure web application with robust software security measures, including file verification via checksums, to protect client data and ensure secure communications.  

To ensure the app was secure, I effectively identified vulnerabilities in Artemis Financial’s software by using tools like OWASP's dependency-check tool to detect issues in third-party libraries,
and I also conducting manual code reviews to uncover insecure coding practices. 
Secure coding is critical to prevent data breaches and protect a company’s reputation, especially when the company handles sensitive financial information.

The most challenging part of the vulnerability assessment was distinguishing false positives in dependency-check reports, which required careful analysis to avoid overlooking real threats. 
However, the dependency-check tool was incredibly helpful, automating vulnerability detection and saving time compared to manual inspections, and its list of known solutions and summaries helped avoid false positives.

It is also important to increase layers of security over time and throughout the development process, as the DevSecOps movement focuses on.
Here, I increased security layers by implementing HTTPS with self-signed certificates, adding checksum verification for data integrity, and refactoring code to address vulnerabilities in dependencies. 
In the future, I would use actual penetration testing to see if there are further vulnerabilities that could be addressed, and it is also important to do periodic checks with
dependancy-check, to catch newly discovered bugs and vulnerabilities.

To ensure the code remained functional and secure after refactoring, I first re-ran dependency-check scans to verify that no new vulnerabilities were introduced, 
ensuring the refactored code maintained security standards. I then did another manual code review and manually checked website performance to see if there were any vulnerabilities. Going forward, it would also be helpful
to introduce more specific unit tests to help with this. 

The most helpful tools from this course that I will use going forward were probably OWASP's dependency-check for vulnerability scanning, Maven for integrating plugins like dependency-check and others,
and Eclipse, which now has its own wide variety of plugins and tools for code review.

To showcase this course to future employers, I would showcase my final report (which is in this github page), showcasing how I was able to understand a client's needs and security requirements,
match those needs to pre-existing hash and encryption algorithms, check and update code to address security concerns and implement the chosen algorithms, and create a full report for management.
