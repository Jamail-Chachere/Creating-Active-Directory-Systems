# Creating-Active-Directory-Systems



<h2>Description</h2>
This project consists creating Active Directory systems. Deploying domain controls and managing different employee accounts.
Also give specific permissions to certain users.
<br />


<h2>Technologies Used</h2>

- <b>Microsoft Azure</b> 
- <b>Windows Remote Desktop</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)
- <b>Windows 10 Server Version</b> 

<h2>Walk-through:</h2>

<p align="center">
We have to create the relevant virtual machines (VMs) in Azure do this this all in the cloud. <br/>
We need to create a Domain controller and a client PC.: <br/>
<img src="https://i.imgur.com/ROHg9zp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Now we have to go into Azure's networking settings a create a static IP. That way our VMs can always communicate with each other.<br/>
  If the IP changes because of it's Dynamic nature the two VMs will not recognize each other. :  <br/>
<img src="https://i.imgur.com/ffwkPkv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 <br/>
<img src="https://i.imgur.com/YXNtIe4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
:  <br/>
<img src="https://i.imgur.com/VEYHBVv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  <br/>
<img src="https://i.imgur.com/BJuFSdZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  Now we ping the Domain Controller (DC) from the Client. We recieved the message "Request timed out" so the ping failed. <br/>
  We now have to change firewall settings to get it working. :  <br/>

<img src="https://i.imgur.com/tutbNMV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  In the domain controller we go to the firewall settings and enable all of the ICMPv4 options. :  <br/>

<img src="https://i.imgur.com/1wv1jJB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<img src="https://i.imgur.com/JzmdnZl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 The ping was successful! Now we stop the ping.:  <br/>
<img src="https://i.imgur.com/24XRwwP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<img src="https://i.imgur.com/azO43WD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 In the domain controller enable the "Active Directory Domain Services) :  <br/>
<img src="https://i.imgur.com/eAO6xzC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Then create a "_ADMINS" folder so we can grant the appropriate permissions to our administrators. :  <br/>
<img src="https://i.imgur.com/UjoOld7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Now we create a user named "jane_admin" as an example. :  <br/>
<img src="https://i.imgur.com/3qP1EFC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  We now add "jane_doe" to the Domain Admins and Domain Users folder. This user now has the appropriate admin privileges! :  <br/>
<img src="https://i.imgur.com/68YN07b.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
