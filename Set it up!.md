# ActiveDirectoryLab
<h1>Set it up! </h1>

<h2>Description</h2>

In this tutorial, the Active Directory home lab is set up with Oracle Virtual Box. The installation of Microsoft Server 2019 as a domain controller and Windows 10 Pro as a client on virtual machines is done. Additionally, the NAT and DHCP are configured to enable the client to connect to the domain. By following this tutorial, you will have the opportunity to learn how to set up an Active Directory home lab, which can be a valuable learning experience for those trying to get into IT field, and anyone interested in networking and virtualization. <br/>

<h2>Languages and Utilities Used</h2>

- <b>[Oracle Virtual Box](https://www.virtualbox.org/)</b>

<h2>Environments Used </h2>

- <b>[Windows server 2019](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-20190)</b> 
- <b>[Windows 10](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-10-enterprise)</b> 
<br/>

![Screenshot](https://github.com/KlaraJansi/ActiveDirectoryLab/blob/main/Pictures/Network%20Map.png)<br/>

<h2>Walk-through:</h2>

<b> Step 1: Install the Oracle Virtual Box <br />

Step 2: Create Windows server 2019 virtual machine <br /> 
![Screenshot](https://github.com/KlaraJansi/ActiveDirectoryLab/blob/main/Pictures/DC%20final.png)

Step 3: Create Windows 10 virtual machine <br /> 
![Screenshot](https://github.com/KlaraJansi/ActiveDirectoryLab/blob/main/Pictures/Client%20final.png)

Step 4: Setup server network adapters </b> <br /> 
-> At the right corner click on  "Network & Internet" <br/>
![Screenshot](https://github.com/KlaraJansi/ActiveDirectoryLab/blob/main/Pictures/AD%20-%20Network%20settings.png) <br/>

-> Click on "Change adapter options" on right side <br/> 

-> Set up IP address for internal network <br />
![Screenshot](https://github.com/KlaraJansi/ActiveDirectoryLab/blob/main/Pictures/AD%20-%20Network%20setiings3.png)<br/>

<b> Step 5: Install Active Directory Domain Services </b> <br />

- Server Manager -> Add roles and features -> Next... -> Role-based or feature-based installation -> Select a server <br/>
![Screenshot](https://github.com/KlaraJansi/ActiveDirectoryLab/blob/main/Pictures/AD%20-%20Adding%20roles.png)<br/>

-> Check the Active Directory Domain Services <br/>
![Screenshot](https://github.com/KlaraJansi/ActiveDirectoryLab/blob/main/Pictures/AD%20-%20Adding%20roles2.png)<br/>

-> Next... -> Install <br />
-> Click on the yellow exclamation mark at the upper right corner <br/>
-> Add a new forest  <br/>
-> name your domain (In this case: 'hackyourlife.com')  <br/>
-> Next... -> set up a password -> Next...  <br/>
-> Install <br />
*you will be logged out <br/>

<b> Step 6: Create admin domain account </b> <br />

-> log in back <br/>
-> Start <br/>
-> Windows Administrative Tools <br/>
-> Active Directory Users and Computers <br/>
-> right click on your domain <br/>
-> New <br/>
-> Organisational Unit <br/>
-> name it '_ADMINS' <br/>
-> Ok <br />
-> right click on '_ADMINS' <br/>
-> New <br/>
-> User <br/>
-> name a admin user <br/>
-> set a password for a user (you can also uncheck 'User must change password at next logon' (just for your convenience) and check 'Password never expires' (if you don't want to deal with that right now) <br />
-> right click on your newly created admin user <br/>
-> Properties <br/>
-> Member Of <br/>
-> Add <br/>
-> Name the new group 'Domain Admins'<br/>
-> Ok <br/>
-> Apply <br/>
* You can now log out and log in back as your new admin account <br />

<b> Step 7: Install and configure RAS/NAT: </b> <br />

-> Add roles and features <br/>
-> Next...  <br/>
-> Remote Access  <br/>
![Screenshot](https://github.com/KlaraJansi/ActiveDirectoryLab/blob/main/Pictures/AD%20-%20Add%20roles%20routing2.png)<br/>
-> Next...  <br/>
-> Check 'Routing'  <br/>
![Screenshot](https://github.com/KlaraJansi/ActiveDirectoryLab/blob/main/Pictures/AD%20-%20Add%20roles%20routing3.png)<br/>
-> Next... 
-> Install <br/>
-> Tools  <br/>
-> Routing and Remote Access  <br/>
-> right click on your domain  <br/>
-> Configure and Enable Routing and Remote Access  <br/>
-> Next...  <br/>
-> Network address translation (NAT)  <br/>
-> Next...  <br/>
-> Use this public interface to connect to the Internet  <br/>
-> select your Internet connection  <br/>
-> Next... <br/>
-> Finish <br/>

<b> Step 8: Install and configure DHCP: </b> <br />

-> Add roles and features <br/>
-> DHCP  <br/>
![Screenshot](https://github.com/KlaraJansi/ActiveDirectoryLab/blob/main/Pictures/AD%20-%20DHCP.png) <br/>

-> Add features <br/>
-> Next... <br/>
-> Install <br/>
-> Tools <br/>
-> DHCP <br/>
-> right click on your domain <br/>
-> New Scope <br/>
![Screenshot](https://github.com/KlaraJansi/ActiveDirectoryLab/blob/main/Pictures/AD%20-DHCP2.png)<br/>
-> Next... <br/>
-> name the scope <br/>
-> set up adress range <br/>
-> Next... <br/>
-> set up Lease duration <br/>
-> Next... <br/>
-> Finish <br/>
-> right click on your domain <br/>
-> Authorize <br/>
-> Refresh <br/>

<b> Step 8: Join your client to domain and login with domain credentials: </b> <br />

-> right click on windows icon <br/>
-> System <br/>
-> Rename your PC (advanced) <br/>
-> Change <br/>
-> Type your domain name and sign in with one of the domain users credentials <br/>
* your network interface on your client should be this: <br/>
![Screenshot](https://github.com/KlaraJansi/ActiveDirectoryLab/blob/main/Pictures/AD%20-client%20network.png) <br/>

<b> All done! </b>


</p>

