<h1>Sniffing Usernames & Passwords From Web Pages & Remote Servers</h1>


<h2>Description</h2>
In this project, we will be exploring how to use Wireshark for sniffing and analyzing network traffic. The goal is to understand the flow of data over unsecured protocols such as FTP and HTTP, which can expose usernames and passwords in plain text. This exercise offers a comprehensive introduction to the basics of network monitoring and packet analysis, demonstrating how easily sensitive information can be intercepted if not properly secured. This setup provides a practical insight into the importance of encryption and secure communication protocols in protecting data integrity and privacy. <br />


<h2>Languages and Utilities Used</h2>

- <b>Wireshark</b> 

<h2>Takeaways</h2>

- <b>Wireshark Packet Sniffing and Analysis</b>: Successfully used Wireshark to capture and analyze network packets, demonstrating the exposure of usernames and passwords transmitted via unencrypted protocols such as FTP and HTTP. This project enhanced understanding of network protocol vulnerabilities and the critical need for secure communications.

- <b>Identification and Analysis of Unsecured Traffic</b>: Gained hands-on experience in identifying and interpreting unsecured traffic patterns, which emphasized the importance of encryption to safeguard data during transmission. This takeaway underscores the significance of deploying secure protocols like HTTPS to prevent data interception and enhance cybersecurity measures.

- <b>Insights into Network Security Measures</b>: Through the direct application of packet sniffing, developed a deeper insight into the practical aspects of cybersecurity, such as the detection of sensitive information in plaintext. This experience highlighted the practical implications of network security, promoting proactive measures to enhance data protection strategies.


<h2>Program walk-through:</h2>

<p align="center">
Sample http website that I will put login details into and will be used for packet sniffing through wireshark: <br/>
<img src="samplesite.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />I used the http filter to narrow the traffic down to show only http packets:  <br/>
<img src="http filter.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
I next used the GET request method filter to help me identify the login request made from the sample website: <br/>
<img src="GET request filter.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
To further narrow down the packet search, I used the POST method request filter to locate the packet containing the form data from the login page on the website:  <br/>
<img src="POST request filter.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
After applying all the necessary filters, we find the packet containing the form data and locate the username and password I created and used to login to the sample website within the bottom left hand side of the screenshot:  <br/>
<img src="UN&P detected.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Getting now into FTP packet analysis, I first used a filter to narrow down traffic that should only be coing through port 21 and is either TCP or FTP:  <br/>
<img src="tcp and port filter.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Since FTP is the main protocol that is to be analyzed here, I used the FTP filter to show only packets containing the FTP protocol :  <br/>
<img src="ftp filter.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
I used a ftp response filter to locate all of the reponse codes sent by the server:  <br/>
<img src="ftp response filter.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Successful verification of code executing and identifying 'admin' as the password stored within the hash:  <br/>
<img src="ftp request arg filter.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Successful verification of code executing and identifying 'admin' as the password stored within the hash:  <br/>
<img src="acc info&actions through tcp stream.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
