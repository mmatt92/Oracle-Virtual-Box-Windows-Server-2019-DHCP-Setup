<h1>Oracle VirtualBox/Windows Server 2019/DHCP Setup</h1>



<h2>Description</h2>

In this lab I configure a DHCP server network within VirtualBox using Windows Server 2019. 
<br />


<h2>Utilities Used</h2>
 
- <b>Oracle VirtualBox</b>

<h2>Environments Used </h2>

- <b>Windows 11</b> 
- <b>Windows Server 2019</b> 

<h2>Starting Windows Server 2019</h2>

<p align="center">
Select Windows Server 2019 and Start virtual machine: <br/>
<img src="https://imgur.com/ATliBcb.png" height="80%" width="80%" alt="Start virtual machine"/>
<br />
<br />
Select Input, Keyboard, Insert Ctrl+Alt+Del from dropdown to unlock:  <br/>
<img src="https://imgur.com/bVf6ySA.png" height="80%" width="80%" alt="Insert Ctrl+Alt+Del"/>
<br />
<br />
Enter password: <br/>
<img src="https://imgur.com/CobmMLI.png" height="80%" width="80%" alt="Enter password"/>
<br/><br/>
Enable Bidirectional Drag and Drop feature to copy and paste from host computer: <br/>
<img src="https://imgur.com/CW1N92R.png" height="80%" width="80%" alt="Click and Drag Your Hardware To the Workspace"/>
<br />
<br />
If Server Manager does not automatically start go to the Windows(Start) icon and select Server Manager: <br/>
<img src="https://imgur.com/jnlmtHe.png" height="80%" width="80%" alt="Server Manager"/>
<br />
<br />
DHCP feature is not enabled by default so you must install it. Select Manage, Add Roles and Features. Select Next for the first three options and choose DHCP Server box: <br />
<img src="https://imgur.com/a5vmtLj.png" height="80%" width="80%" alt="DHCP is not enabled"/>
<img src="https://imgur.com/iFOuSkn.png" height="80%" width="80%" alt="DHCP is not enabled"/>
<br />
<br />
Click on Add Features then Next three more times and Install: <br />
<img src="https://imgur.com/JUNKma3.png" height="80%" width="80%" alt="Add Features"/>
<img src="https://imgur.com/txTuERA.png" height="80%" width="80%" alt="Install"/>
<br />
<br />
It may take a few minutes to install depending on the speed of your virtual machine. When finished select Close:  <br />
<img src="https://imgur.com/xbFcbLB.png" height="80%" width="80%" alt="minute to install"/>
<br />
<br />
Now select Tools and verify the DHCP feature was installed then click on DHCP: <br />
<img src="https://imgur.com/a9c58nH.png" height="80%" width="80%" alt="verify the DHCP feature was installed"/>
<img src="https://imgur.com/oKtUr9N.png" height="80%" width="80%" alt="click on DHCP"/>
<br />
<br />
Next click the IPv4, Server Options, More Actions, and Configure Options: <br />
<img src="https://imgur.com/Nh7ew1k.png" height="80%" width="80%" alt="Server Options"/>
<br />
<br />
Next select the 005 Name Server, enter the IP address as 192.168.20.1, Add, then OK: <br />
<img src="https://imgur.com/RLssRyR.png" height="80%" width="80%" alt="005 Name Server"/>
<br />
<br />
Now to set a new Scope. Right click on the IPv4 server and select New Scope, click Next, name the network, and Next: <br />
<img src="https://imgur.com/t2LWRSj.png" height="80%" width="80%" alt="New Scope"/>
<img src="https://imgur.com/YSovXSd.png" height="80%" width="80%" alt="New Scope"/>
<img src="https://imgur.com/Tj2wBk0.png" height="80%" width="80%" alt="New Scope"/>
<br />
<br />
I set the Start IP to 192.168.20.50 and the End IP to 192.168.20.250, then Next: <br />
<img src="https://imgur.com/D7Imq66.png" height="80%" width="80%" alt="Set Start and End IP"/>
<br />
<br />
Set a range of Exclusions Starting at 192.168.20.100 and Ending at 192.168.20.125 for a camera system, then Next: <br />
<img src="https://imgur.com/Al7oaH5.png" height="80%" width="80%" alt="Exclusions"/>
<br />
<br />
Next you can change your Lease Duration depending on your environment, but I chose to leave mine at 8 days: <br />
<img src="https://imgur.com/c3FO2Sb.png" height="80%" width="80%" alt="change your Lease Duration"/>
<br />
<br />
Next you can choose to Configure DHCP Options now or later, I select later, and click Finish: <br />
<img src="https://imgur.com/QOo5oDl.png" height="80%" width="80%" alt="Configure DHCP Options"/>
<br />
<br />
Scope is now added to IPv4: <br />
<img src="https://imgur.com/docTO9e.png" height="80%" width="80%" alt="Scope is now added to IPv4"/>
<br />
<br />
Select Address Pool to see Address range and Exclusions set earlier: <br />
<img src="https://imgur.com/6PiBzkv.png" height="80%" width="80%" alt="Select Address Pool"/>
<br />
<br />
Address Leases is where your connected devices will show: <br />
<img src="https://imgur.com/Yi7oj8f.png" height="80%" width="80%" alt="Address Leases"/>
<br />
<br />
Reservations will show here, reserving an IP address for a particular MAC addess: <br />
<img src="https://imgur.com/f3GLI3h.png" height="80%" width="80%" alt="Reservations"/>
<br />
<br />
Next right click on Scope Options and select Configure Options. Select Router and Add IP 192.168.20.254: <br />
<img src="https://imgur.com/hkf3Eoh.png" height="80%" width="80%" alt="Scope Options"/>
<img src="https://imgur.com/7yqrgWQ.png" height="80%" width="80%" alt="Configure Options"/>
<img src="https://imgur.com/fmdAKmX.png" height="80%" width="80%" alt="Select Router"/>
<br />
<br />
Next I will go back to Configure Options and Select 006 DNS Servers. Assign it an address of 1.1.1.1: <br />
<img src="https://imgur.com/uYV3EpK.png" height="80%" width="80%" alt="Configure Options"/>
<img src="https://imgur.com/wMFsrRv.png" height="80%" width="80%" alt="DNS Servers"/>
<br />
<br />
After final configurations on a real setup computers would now be able to connect to this nework, obtain an IP address automatically from the DHCP server, and search the web utilizing the DNS server: <br />
<img src="https://imgur.com/bycb2Br.png" height="80%" width="80%" alt="Configure Options"/>
<br />
<br />
END OF LAB


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

