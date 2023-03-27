# ActiveDirectoryLab
<h1> Add User, Group, Organizational Unit </h1>

<h2>Description</h2>

This guide provides a step-by-step walkthrough for adding users, groups, and organizational units in a virtual machine homelab environment of Active Directory. The guide includes detailed instructions and screenshots to help users easily navigate the process and successfully set up their Active Directory environment.
<h2>Languages and Utilities Used</h2>

- <b>[Oracle Virtual Box](https://www.virtualbox.org/)</b>

<h2>Environments Used </h2>

- <b>[Windows server 2019](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-20190)</b> 
- <b>[Windows 10](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-10-enterprise)</b> 
<br/>

![Screenshot](https://github.com/KlaraJansi/ActiveDirectoryLab/blob/main/Pictures/Network%20Map.png)<br/>

<h2>Walk-through:</h2>

<b> Add User </b> <br/>
Go to 'Tools' -> AD Users and Computers -> click on your domain -> Users -> right click -> New -> User <br/>
![Screenshot](https://github.com/KlaraJansi/ActiveDirectoryLab/blob/main/Pictures/New%20User.png)
  
 <b> Set-up password </b> <br/>
When setting password you have few more options: for training purpose you can unmark 'user must change password on next logon'<br/>
 ![Screenshot](https://github.com/KlaraJansi/ActiveDirectoryLab/blob/main/Pictures/New%20User%20-Password.png) 
  
 <b> User properties </b> <br/> 
 As you can see in the images below, you can choose to add bunch of things for the user: address, phone, email, department, etc. <br/>
 ![Screenshot](https://github.com/KlaraJansi/ActiveDirectoryLab/blob/main/Pictures/User%20-%20properties.png)
 ![Screenshot](https://github.com/KlaraJansi/ActiveDirectoryLab/blob/main/Pictures/User-properties%202.png)
   
 <b> Add Group </b> <br/> 
 Add group is similar as Add user ... -> New -> Group <br/> 
 There is a difference betwewen 'Security' and 'Distribution' Group. Security Group is used to assign permissions to shared resources and Distribution Group is used to create email distribution lists. <br/>
 
 You can also choose the scope of the group. The scope of an AD group determines both where the group can be applied in the forest or domain and who can be a member of a group. Because Active Directory has few limitations on how groups can be nested within each other, group nesting can present massive security and operational risks to an organization. The only real help that AD offers to combat the risks of nesting security groups is group scope.<br/>
 
 Universal scope: Group can be assigned permissions in any domain or forest <br/>
 Global scope: Member permissions can be assigned in any domain <br/>
 Domain Local scope: Member permissions can be assigned only within the same domain as the parent domain local group <br/

![Screenshot](https://github.com/KlaraJansi/ActiveDirectoryLab/blob/main/Pictures/Group.png)
To add user to group, just click on 'Members' -> add -> add your user and save <br/>
![Screenshot](https://github.com/KlaraJansi/ActiveDirectoryLab/blob/main/Pictures/Group%20member.png)

<b> Folder sharing </b> <br/>
Add a new folder on your desktop -> right click -> properties -> share -> advance sharing -> add your user, you can choose between full control over the file or just, change or read
![Screenshot](https://github.com/KlaraJansi/ActiveDirectoryLab/blob/main/Pictures/Folder%20share.png) <br/>
![Screenshot](https://github.com/KlaraJansi/ActiveDirectoryLab/blob/main/Pictures/Folder%20-%20permissions.png)<br/>
![Screenshot](https://github.com/KlaraJansi/ActiveDirectoryLab/blob/main/Pictures/Folder%20-%20full%20control%20acccess%20for%20user.png)<br/>

<b> All done! </b>




