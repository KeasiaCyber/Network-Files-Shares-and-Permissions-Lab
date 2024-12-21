# Network-Files-Shares-and-Permissions-Lab

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Installation Steps</h2>

<p>
<img src="https://imgur.com/5B3iQlN.png" height="80%" width="80%" alt="Steps 1"/>
</p>
<p>
Hello !, so today were going to work on sharing files over a network and setting permission for them. Okay so create 4 folders name "read-access,write-access,no access and accounting".
</p>
<br />

<p>
<img src="https://imgur.com/Z8evmOo.png" height="80%" width="80%" alt="Steps 2"/>
</p>
<p>
Set permission to the read, write and no access folders. choose which domain uses what for example domain admin will be set to no access folder so they are only ones that can access that folder, while the other folders only can be access to the domain user.
</p>
<br />

<p>
<img src="https://imgur.com/GkA3vCP.png" height="80%" width="80%" alt="Steps 3"/>
</p>
<p>
Lets head to our cilent 1 vm and see if those folders pop up. which they will but you only have access to any other folder except no access folder.
</p>
<br />

<p>
<img src="https://imgur.com/vE0pkir.png" height="80%" width="80%" alt="Steps 4"/>
<img src="https://imgur.com/JhgP08s.png" height="80%" width="80%" alt="Steps 5"/>
<img src="https://imgur.com/JhgP08s.png" height="80%" width="80%" alt="Steps 6"/>
</p>
<p>
Start by creating a security group named "ACCOUNTANTS" in Active Directory on DC-1. Then, navigate to the "accounting" folder created earlier and assign the group "ACCOUNTANTS" the Read/Write permissions for the folder.
</p>
<br />

<p>
<img src="https://imgur.com/nCvNlaa.png" height="80%" width="80%" alt="Steps 6"/>
</p>
<p>
Test the setup by signing into Client-1 as <someuser> and attempting to access the "accounting" folder. Initially, this attempt should fail. Next, log out of Client-1 and return to DC-1, where you'll add user to the "ACCOUNTANTS" security group. Finally, sign back into Client-1 as user and try accessing the "accounting" share again at \\DC-1\. Verify whether the permissions now allow access.
</p>
<br />
