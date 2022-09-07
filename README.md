# ActiveDirectoryLab
<h1>Set it up! </h1>

<h2>Description</h2>
This is tutorial for set up the Active Directory Home Lab with Oracle Virtual Box. I installed Microsoft server 2019 as a domain controller and Windows 10 pro as a client. I also configured NAT and DHCP to be able to connect my client to domain. 
<br />

<h2> Watch a video walkthrough! </h2> 

<---in progress--->

<h2>Languages and Utilities Used</h2>

- <b>[Oracle Virtual Box](https://www.virtualbox.org/)</b>


<h2>Environments Used </h2>

- <b>[Windows server 2019](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-20190)</b> 
- <b>[Windows 10](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-10-enterprise)</b> 

<h2>Walk-through:</h2>

<b> Step 1: Install the Oracle Virtual Box <br />
Step 2: Create Windows server 2019 virtual machine <br /> 
Step 3: Create Windows 10 virtual machine <br /> 
Step 4: Setup server network adapters </b> <br /> 
- Settings -> Network & Internet -> Change adapter options -> Set up IP address for internal network <br />

<b> Step 5: Install Active Directory Domain Services </b> <br />
- Server Manager -> Add roles and features -> Next... -> Role-based or feature-based installation -> Select a server -> Check the Active Directory Domain Services -> Next... -> Install <br />
- Click on the yellow exclamation mark  <br />
- Add a new forest -> name your domain -> Next... -> set up a password -> Next... -> Install <br />
*you will be logged out 

<b> Step 6: Create admin domain account </b> <br />
- log in back -> Start -> Windows Administrative Tools -> Active Directory Users and Computers -> right click on your domain -> New -> Organisational Unit -> name it '_ADMINS' -> Ok <br />
- right click on '_ADMINS' -> New -> User -> name a admin user -> set a password for a user (you can also uncheck 'User must change password at next logon' and check 'Password never expires', if you don't want to deal with that right now) <br />
- right click on your newly created admin user -> Properties -> Member Of -> Add -> Name the new group 'Domain Admins' -> Ok -> Apply 
* You can now log out and log in back as your new admin account <br />

<b> Step 7: Install and configure RAS/NAT: </b> <br />
- Add roles and features -> Next... -> Remote Access -> Next... -> Check 'Routing' -> Next... -> Install
- Tools -> Routing and Remote Access -> right click on your domain -> COnfigure and Enable Routing and Remote Access -> Next... -> Network address translation (NAT) -> Next... -> Use this public interface to connect to the Internet -> select your Internet connection -> Next... -> Finish

<b> Step 8: Install and configure DHCP: </b> <br />
- Add roles and features -> DHCP -> Add features -> Next... -> Install
- Tools -> DHCP -> right click on your domain -> New Scope -> Next... -> name the scope -> set up adress range -> Next... -> set up Lease duration -> Next... -> Finish
- right click on your domain -> Authorize -> Refresh

<b> Step 8: Join your client to domain and login with domain credentials: </b> <br />
- right click on windows icon -> System -> Rename your PC (advanced) -> Change -> Type your domain name and sign in with one of the domain users credentials

<b> All done! </b>

</p>

