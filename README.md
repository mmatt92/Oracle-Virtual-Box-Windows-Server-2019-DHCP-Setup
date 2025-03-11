<h1>Oracle VirtualBox/Windows Server 2019/DHCP Setup</h1>



<h2>Description</h2>

In this lab I configure a DHCP server network within VirtualBox using Windows Server 2019. This assumes you have already downloaded and installed VirtualBox and Windows Server with user interface. 
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
<br/>
<br/>
Enable Bidirectional Drag and Drop feature to copy and paste from host computer: <br/>
<img src="https://imgur.com/CW1N92R.png" height="80%" width="80%" alt="Click and Drag Your Hardware To the Workspace"/>
<br />
<br />
Label the two PCs PC1 and PC2: <br/>
<img src="https://imgur.com/W8h097p.png" height="80%" width="80%" alt="Click and Drag Your Hardware To the Workspace"/>
<br />
<br />
Next add switches: <br />
<img src="https://imgur.com/s9jQiBR.png" height="80%" width="80%" alt="Click and Drag Your Hardware To the Workspace"/>
<img src="https://imgur.com/5h2Ecvu.png" height="80%" width="80%" alt="Click and Drag Your Hardware To the Workspace"/>
<br />
<br />
Label switches S1 and S2: <br />
<img src="https://imgur.com/zSnkvZP.png" height="80%" width="80%" alt="Click and Drag Your Hardware To the Workspace"/>
<br />
<br />
Next add routers:  <br />
<img src="https://imgur.com/pwyibnt.png" height="80%" width="80%" alt="Click and Drag Your Hardware To the Workspace"/>
<img src="https://imgur.com/BmyY5OI.png" height="80%" width="80%" alt="Click and Drag Your Hardware To the Workspace"/>
<br />
<br />
Label routers NY and LA: <br />
<img src="https://imgur.com/zJYgsIt.png" height="80%" width="80%" alt="Click and Drag Your Hardware To the Workspace"/>
<br />
<br />
Next add cable to connect devices: <br />
<img src="https://imgur.com/2L5GC8d.png" height="80%" width="80%" alt="Add Cable to Connect Devices"/>
<img src="https://imgur.com/N5EIW08.png" height="80%" width="80%" alt="Add Cable to Connect Devices"/>
<br />
<br />
Cable is connected to PC1 Fast Ethernet Port then to S1 Fast Ethernet 0/2: <br />
<img src="https://imgur.com/hvNCEpd.png" height="80%" width="80%" alt="Add Cable to Connect Devices"/>
<img src="https://imgur.com/IG0b3QF.png" height="80%" width="80%" alt="Add Cable to Connect Devices"/>
<br />
<br />
Next connect Fast Ethernet Port 0/1 on S1 to Gigabit Ethernet Port 0/1 on NY router: <br />
<img src="https://imgur.com/T9IS4D7.png" height="80%" width="80%" alt="Add Cable to Connect Devices"/>
<img src="https://imgur.com/TcIIGKy.png" height="80%" width="80%" alt="Add Cable to Connect Devices"/>
<img src="https://imgur.com/OHriMNx.png" height="80%" width="80%" alt="Add Cable to Connect Devices"/>
<br />
<br />
PC2 is then connected to S2 with Fast Ethernet 0 to Fast Ethernet 0/2 on the switch: <br />
<img src="https://imgur.com/0RoVcqc.png" height="80%" width="80%" alt="Add Cable to Connect Devices"/>
<img src="https://imgur.com/0qv9dea.png" height="80%" width="80%" alt="Add Cable to Connect Devices"/>
<img src="https://imgur.com/c9Z8u7y.png" height="80%" width="80%" alt="Add Cable to Connect Devices"/>
<br />
<br />
Next S1 Fast Ethernet 0/1 is connected to LA Router Gigabit Ethernet 0/1: <br />
<img src="https://imgur.com/pgNPEdb.png" height="80%" width="80%" alt="Add Cable to Connect Devices"/>
<img src="https://imgur.com/tnJkZkG.png" height="80%" width="80%" alt="Add Cable to Connect Devices"/>
<img src="https://imgur.com/ckIfNsr.png" height="80%" width="80%" alt="Add Cable to Connect Devices"/>
<br />
<br />
Routers NY Gigabit Ethernet 0/0 and LA Gigabit Ethernet 0/0 are connected: <br />
<img src="https://imgur.com/rDlcdBN.png" height="80%" width="80%" alt="Add Cable to Connect Devices"/>
<img src="https://imgur.com/zDliCFn.png" height="80%" width="80%" alt="Add Cable to Connect Devices"/>
<img src="https://imgur.com/OS7nKFr.png" height="80%" width="80%" alt="Add Cable to Connect Devices"/>
<br />
<br />
Next start to configure the equipment starting with PC1: <br />
<img src="https://imgur.com/h1y6MZ4.png" height="80%" width="80%" alt="Configure the Equipment"/>
<img src="https://imgur.com/o9hEwVB.png" height="80%" width="80%" alt="Configure the Equipment"/>
<img src="https://imgur.com/H7NAQHO.png" height="80%" width="80%" alt="Configure the Equipment"/>
<img src="https://imgur.com/ujEzeQv.png" height="80%" width="80%" alt="Configure the Equipment"/>
<img src="https://imgur.com/uRoY1bZ.png" height="80%" width="80%" alt="Configure the Equipment"/>
<br />
<br />
Continue to configure with PC2: <br />
<img src="https://imgur.com/goCyCie.png" height="80%" width="80%" alt="Configure the Equipment"/>
<img src="https://imgur.com/gduJLis.png" height="80%" width="80%" alt="Configure the Equipment"/>
<img src="https://imgur.com/SWya8cU.png" height="80%" width="80%" alt="Configure the Equipment"/>
<img src="https://imgur.com/bMaCzfP.png" height="80%" width="80%" alt="Configure the Equipment"/>
<img src="https://imgur.com/Ha5Et8O.png" height="80%" width="80%" alt="Configure the Equipment"/>
<br />
<br />
Now I will configure the NY router using the command line: <br />
<img src="https://imgur.com/aae7ys4.png" height="80%" width="80%" alt="Configure the Equipment"/>
<img src="https://imgur.com/RUJck1Y.png" height="80%" width="80%" alt="Configure the Equipment"/>
<br />
<br />
Enter "enable" then enter to gain full functionality of router: <br />
<img src="https://imgur.com/5zWX6H4.png" height="80%" width="80%" alt="Configure the Equipment"/>
<br />
<br />
Next enter configuration terminal or "config t" enter. Then assign router name by entering "hostname NY" enter: <br />
<img src="https://imgur.com/Yvq7CbR.png" height="80%" width="80%" alt="Configure the Equipment"/>
<br />
<br />
Now configure interface port g0/1 of router following network map: <br />
<img src="https://imgur.com/XsrzsZe.png" height="80%" width="80%" alt="Configure the Equipment"/>
<img src="https://imgur.com/wg1pa4a.png" height="80%" width="80%" alt="Configure the Equipment"/>
<br />
<br />
Next enable communication with g0/1 interface port by entering command "no shutdown" enter. A green arrow should appear showing connection: <br />
<img src="https://imgur.com/DCk72gv.png" height="80%" width="80%" alt="Configure the Equipment"/>
<img src="https://imgur.com/T46NlIH.png" height="80%" width="80%" alt="Configure the Equipment"/>
<br />
<br />
Now configure interface port g0/0 of router following network map. First enter "exit" to reset. Then interface and enter IP and Subnet. Then use "no shutdown" again to enable communication. Arrow on map will remain red until LA router is configured: <br />
<img src="https://imgur.com/XsrzsZe.png" height="80%" width="80%" alt="Configure the Equipment"/>
<img src="https://imgur.com/4j4abdr.png" height="80%" width="80%" alt="Configure the Equipment"/>
<img src="https://imgur.com/vgxhejp.png" height="80%" width="80%" alt="Configure the Equipment"/>
<br />
<br />
Now configure the LA router using the command line: <br />
<img src="https://imgur.com/n1o8s4i.png" height="80%" width="80%" alt="Configure the Equipment"/>
<img src="https://imgur.com/RUJck1Y.png" height="80%" width="80%" alt="Configure the Equipment"/>
<br />
<br />
Enter "enable" then enter to gain full functionality of router: <br />
<img src="https://imgur.com/5zWX6H4.png" height="80%" width="80%" alt="Configure the Equipment"/>
<br />
<br />
Next enter configuration terminal or "config t" enter. Then assign router name by entering "hostname LA" enter: <br />
<img src="https://imgur.com/SfbcsTF.png" height="80%" width="80%" alt="Configure the Equipment"/>
<br />
<br />
Now configure interface port g0/1 of router following network map. Then enter "no shutdown" command: <br />
<img src="https://imgur.com/kToqyJf.png" height="80%" width="80%" alt="Configure the Equipment"/>
<img src="https://imgur.com/6pPKoCf.png" height="80%" width="80%" alt="Configure the Equipment"/>
<br />
<br />
Now configure interface Port g0/0 of router following network map. First enter "exit" to reset interface then enter IP and Subnet. Then use "no shutdown" again to enable communication. Arrows should now be green showing connection: <br />
<img src="https://imgur.com/cLP22Hg.png" height="80%" width="80%" alt="Configure the Equipment"/>
<img src="https://imgur.com/wnyWjla.png" height="80%" width="80%" alt="Configure the Equipment"/>
<img src="https://imgur.com/4omHNYb.png" height="80%" width="80%" alt="Configure the Equipment"/>
<br />
<br />
Now verify the NY router can ping all of the available networks. Start by clicking on NY router and going to its CLI: <br />
<img src="https://imgur.com/L7b4jps.png" height="80%" width="80%" alt="Now verify the routers"/>
 <br />
<br />
Type "enable" enter, "show ip route" enter. Notice 192.168.10.0 and 192.168.20.0 are the only networks visible to router currently:  <br/>
<img src="https://imgur.com/zjDVXa3.png" height="80%" width="80%" alt="Follow Prompts on Screen"/>
<br />
<br />
This is currently all the router can see. 192.168.30.0 network is on the LA router:  <br/>
<img src="https://imgur.com/NUCSzzH.png" height="80%" width="80%" alt="This is currently all the router can see"/>
<br />
<br />
Using the command line on the NY router type "config t" enter, "ip route 192.168.30.0 255.255.255.0 192.168.20.2" enter. This will instruct NY router to send packets destined for 192.168.30.0 to the LA Router:  <br/>
<img src="https://imgur.com/0DOLR1V.png" height="80%" width="80%" alt="Using the command line on the NY router"/>
<img src="https://imgur.com/0sh0iQ7.png" height="80%" width="80%" alt="Using the command line on the NY router"/>
<br />
<br />
To verify type "do show ip route" enter. Notice that the 192.168.30.0 network is visible to the NY router:  <br/>
<img src="https://imgur.com/3GPunhU.png" height="80%" width="80%" alt="To verify type"/>
<br />
<br />
Now verify the LA router can ping all of the available networks. Start by clicking on LA router and going to its CLI: <br />
<img src="https://imgur.com/kH0usyF.png" height="80%" width="80%" alt="Follow Prompts on Screen"/>
<img src="https://imgur.com/fT40gAd.png" height="80%" width="80%" alt="Follow Prompts on Screen"/>
<br />
<br />
To verify type "enable" enter "show ip route" enter. Notice 192.168.20.0 and 192.168.30.0 are the only networks visible to router currently:  <br/>
<img src="https://imgur.com/2YXQgHJ.png" height="80%" width="80%" alt="To verify type"/>
<br />
<br />
The 192.168.10.0 network is on the NY router:  <br/>
<img src="https://imgur.com/PDm0wpP.png" height="80%" width="80%" alt="This is currently all the router can see"/>
<br />
<br />
Using the command line on the LA router type "config t" enter, "ip route 192.168.10.0 255.255.255.0 192.168.20.1" enter. This will instruct NY router to send packets destined for 192.168.10.0 to the NY Router:  <br/>
<img src="https://imgur.com/OrwFHqa.png" height="80%" width="80%" alt="Using the command line on the NY router type"/>
<br />
<br />
Now we need to verify PC1 can ping PC2 starting with 192.168.20.2 then 192.168.30.1 and finally 192.168.30.10:  <br/>
<img src="https://imgur.com/u1jiWtD.png" height="80%" width="80%" alt="To verify type"/>
<img src="https://imgur.com/pCF1kUN.png" height="80%" width="80%" alt="To verify type"/>
<img src="https://imgur.com/G7Qj2yF.png" height="80%" width="80%" alt="To verify type"/>
<img src="https://imgur.com/0XXlGoi.png" height="80%" width="80%" alt="To verify type"/>
<img src="https://imgur.com/9Jy85yJ.png" height="80%" width="80%" alt="To verify type"/>
<br />
<br />
PC1 can now successfully ping 192.168.30.10. Ping serves as an echo so PC2 should ping back with no problem but to verify go to PC2 CMD prompt and enter 192.168.10.10:  <br/>
<img src="https://imgur.com/X0jHef7.png" height="80%" width="80%" alt="To verify type"/>
<img src="https://imgur.com/zI1ySoE.png" height="80%" width="80%" alt="To verify type"/>
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

