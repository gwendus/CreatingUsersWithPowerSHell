<p align="center">

<img src="https://upload.wikimedia.org/wikipedia/commons/2/2f/PowerShell_5.0_icon.png" alt="PowerShell"/>
 
 <h1>#CreatingUsersWithPowerShell</h1>
This tutorial outlines the use of PowerShell and basic scripting to create 1000 users for our Active Directory Environment.
<br />


<h2>Environments and Technologies</h2>

- <b>Microsoft Azure</b> 
- <b>Remote Desktop</b>
- <b>PowerShell</b>

<h2>Operating Systems</h2>

- <b>Windows 10</b> (22H2)
- <b>Windows Server</b> (2022)
  <br />

<h2>Setting Up Remote Desktop for non-administrative users on Client-1:</h2>
Log into Client-1 as mydomain.com\jane_admin.
  <br>
  <br>
<img src="https://i.imgur.com/RdOEPwE.png" height="80%" width="80%" alt="login as Jane Admin"/>
<br />
<br />

Right click the Start menu and select "System" to access settings. Select "Remote Desktop."

<img src="https://i.imgur.com/LFFpl5z.png" height="80%" width="80%" alt="Select Remote Desktop"/><br />
<br />
<br />

Allow “domain users” access to remote desktop. Apply the changes. You can now log into Client-1 as a normal, non-administrative user now.

<img src="https://i.imgur.com/JOKH06b.png" height="80%" width="80%" alt="Allow Domain Users"/>

<br />
<br />

<h2>Creating Users with PowerShell scripting</h2>

Log into DC-1 as jane_admin. Open PowerShell_ise *as an administrator*. <br/>

<img src="https://i.imgur.com/0WdwokK.png" height="80%" width="80%" alt="Open PowerShell as an Admin"/>
<br />
<br />

Create a new File and paste the contents of the <a href="https://github.com/joshmadakor1/AD_PS/blob/master/Generate-Names-Create-Users.ps1)/">script</a> into it. Copy the raw file, create a new file (far left) save with ctrl + s or the save button, name it "create users," and press Run. <br>
<br />
<img src="https://i.imgur.com/k9xU9GA.png" height="80%" width="80%" alt="C&P script"/>

<br />
<br />

Observe the script running. This will create 1000 users within the appropriate OU.
  <br>
<br/>
<img src="https://i.imgur.com/f0YhU1U.png" height="80%" width="80%" alt="Observe the script running"/>
<br />
<br />

When finished, open ADUC and observe the accounts in the appropriate OU (_EMPLOYEES).
<br/>
<img src="https://i.imgur.com/RPDbOfY.png" height="80%" width="80%" alt="OU emplyees created"/>
<br />
<br />

Attempt to log into Client-1 with one of the accounts (take note of the password in the script). Success!
<br/>

<img src="https://i.imgur.com/81qLEgq.png" height="80%" width="80%" alt="Success!"/>
<br />
<br />


Finish the lab, but do not delete the VMs in Azure. We will use them for upcoming labs.
If you are done for the day and want to save money, simply “Stop”/turn off the VMs within the Azure Portal
<br/>

<img src="https://i.imgur.com/ZpjzuJm.png" height="70%" width="70%" alt="Register new PHP version."/>
<br />
<br />

Finish the lab, but do not delete the VMs in Azure. We will use them for upcoming labs.
If you are done for the day and want to save money, simply “Stop”/turn off the VMs within the Azure Portal
