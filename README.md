<h1>Sniffing Usernames & Passwords From Web Pages & Remote Servers</h1>


<h2>Description</h2>
In this project, we will be exploring how to use Wireshark for sniffing and analyzing network traffic. The goal is to understand the flow of data over unsecured protocols such as FTP and HTTP, which can expose usernames and passwords in plain text. This exercise offers a comprehensive introduction to the basics of network monitoring and packet analysis, demonstrating how easily sensitive information can be intercepted if not properly secured. This setup provides a practical insight into the importance of encryption and secure communication protocols in protecting data integrity and privacy. <br />


<h2>Languages and Utilities Used</h2>

- <b>Wireshark</b> 

<h2>Takeaways</h2>

- <b>Python Script Development for MD5 Hash Cracking</b>: Successfully developed a Python script that deciphers MD5 hashes to reveal plain text passwords, emphasizing practical applications of cryptographic techniques. Demonstrated proficiency in utilizing Python's hashlib module, enhancing skills in creating security tools and understanding hash function vulnerabilities.

- <b>Testing and Verification of Script Functionality</b>: Acquired practical experience by rigorously testing the hash cracker against a custom password list, validating the script’s effectiveness in identifying the correct passwords. This process highlighted the importance of comprehensive testing in software development, ensuring the tool’s functionality and reliability in real-world scenarios.


<h2>Program walk-through:</h2>

<p align="center">
Python script code for MD5 hash cracker using nano text editor: <br/>
<img src="Python code.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />Created a .txt file containing list of possible passwords:  <br/>
<img src="list of passwords.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Generated an MD5 hash tied to the password 'admin': <br/>
<img src="md5 hash example.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Successful verification of code executing and identifying 'admin' as the password stored within the hash:  <br/>
<img src="verfication.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
</p>


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
