LAN-HARDENING: PORT-SECURITY



## Key features of the implementation include:

-<b>Cisco switch 2960<b/>

-<b>Personal Computers(PC's)<b/>

-<b>Straight Through Cables(STP)<b/>



This repository serves as a practical showcase of PORT SECURITY, virtualization strategy, and access control implementation—ideal for IT professionals, students, and cybersecurity enthusiasts.
<br />





<h2>Project walk-through:</h2>

<p align="center">
Network Diagram: <br/>
<img src="https://imgur.com/0uNYwqr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  <br/>
<img src="https://imgur.com/Fg5D0JQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  <br/>
<img src="https://imgur.com/6P0G9J2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  <br/>
<img src="https://imgur.com/u4m6gYQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  <br/>
<img src="https://imgur.com/3tw7tHc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 <br/>
<img src="https://imgur.com/Di2VSnp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  <br/>
<img src="https://imgur.com/j02Exs1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 <br/>
<img src="https://imgur.com/jgutBjQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  <br/>
<img src="https://imgur.com/l2htqlh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  <br/>
<img src="https://imgur.com/T1vsxHL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
</p>

<h2>Conclusion</h2> ## Conclusion

The successful implementation of Port Security on the Cisco 2960 switch marks a critical step in hardening the Local Area Network (LAN). By moving away from a default "plug-and-play" configuration, we have established a controlled environment where the physical access layer is actively defended against unauthorized intrusions.

### Summary of Achievements:
* **MAC Address Control:** By utilizing `switchport port-security mac-address sticky`, the network now dynamically learns and persists authorized hardware addresses, preventing rogue device connectivity.
* **Attack Mitigation:** The configuration effectively mitigates Layer 2 threats such as CAM Table Overflows and MAC Spoofing by enforcing strict limits on the number of devices per interface.
* **Automated Incident Response:** Through the use of the `shutdown` violation mode, the infrastructure is now capable of self-healing and immediate threat isolation without manual administrator intervention.
* **Network Visibility:** The implementation provides improved audit trails, allowing IT teams to identify exactly which port was breached and which unauthorized device triggered the security event.

### Final Thoughts:
This project demonstrates that LAN hardening is not a one-time setup but a continuous strategy of access control. While this lab focuses on port-level security, it serves as the foundation for higher-level implementations such as 802.1X authentication and Dynamic ARP Inspection (DAI), ensuring a robust "Defense in Depth" posture for the enterprise.

<br>
<br />
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
