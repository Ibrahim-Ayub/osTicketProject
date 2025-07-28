<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket from Installation to Demo</h1>



### [<h2>Video Demonstration</h2>](https://www.youtube.com/watch?v=fAfp3UmocsQ&t=7s)
This tutorial demonstrates the ticketing system after it has been installed and configured. The demo shows how to create "fake tickets" and illustrates how someone working in a help desk would utilize a ticket system to manage and resolve tickets.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- osTicket

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Have a laptop with internet connection
- Have a Azure account with active subscription




<h2>osTicket Installation Steps</h2>

<p>
<img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/9fe4ef22-2ecb-426b-977c-0cba88327c01" />   
</p>

<p>
The picture above shows the creation of the resource group that will be used for this project. The purpose of this resource group is to manage and organize our resources efficiently.
</p>
<br />

<p>
<img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/c7af2a69-38db-4319-98d5-97185ca23ca3" /> <img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/9da0d795-48f4-4b17-9918-3f97b8120c5f" />
</p>

<p>
The picture above shows the creation of the virtual machine that will be used for this project. This is the machine where osTicket will be installed and configured. You can see that the machine we will be working on is a Windows 10 machine with 4vcpus and 16 GB of memory. The following picture shows the VM after it's been created with its public IP Address. This is the public IP address we will use to connect to the VM remotely using Remote Desktop Connection.  
</p>
<br />

<p>
<img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/6fe3b236-a952-4564-a315-896373dda0d2" />
</p>

<p>
The image above shows all the installation files we will need to download for osTicket. Some of these files are required for osTicket, while others are dependencies necessary for the software to function.
</p>
<br />

<p>
<img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/5fce38dd-01e5-4e27-9dbe-6dd21ae3eb00" />
</p>

<p>
The image above shows me installing CGI and enabling IIS. To install, open the Control Panel and go to Uninstall Programs. From there, on the left, click Turn Windows Features on or off. Click the IIS Box. World Wide Web Services -> Application Development Features -> CGI.
</p>
<br />

<p>
<img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/8dba765e-6146-4264-9a0b-aff8071d31d1" /> <img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/811b0434-47fb-483e-82de-f4e96dff7902" />
</p>

<p>
The images above show me installing some of the dependencies from the folder where all the installation files were. Click the PHP manager file and the Rewrite Module, and then install both files. 
</p>
<br />

<p>
<img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/db640b1a-f816-47ff-b24b-c7380352d668" />
</p>

<p>
The image above shows the PHP 7.3.8 unzipped in a PHP folder on the Windows C Drive. Open File Explorer, navigate to this PC, then click your C drive. In the C drive, create a new folder called PHP. Then, from the osTicket installation files, unzip the PHP 7.3.8 file and move it into the newly created PHP file on the C drive. 
</p>
<br />

<p>
<img width="80% height="80%" alt="image" src="https://github.com/user-attachments/assets/025618c7-6fd5-456a-89f2-796ae20c7b7d" /> <img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/b3495114-170e-4f53-a511-5f2cfc26644f" />
</p>

<p>
The images above show me downloading dependencies from the OS Ticket Installation files. Click on the VC_redist file to install it. Then, for the SQL file, click on it to install, but you will need to select some options. Make sure to click Typical Setup -> Launch Configuration Wizard (after installation) -> Standard Configuration -> Username: root, Password: root.
</p>
<br />

<p>
<img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/6ddb2165-c448-4f3f-a6bb-f6964f22c76c" />
</p>

<p>
The image above shows PHP registered from within IIS. To perform this search, type 'IIS' in the Windows search bar and open it as an administrator. You should see the PHP manager once IIS is opened up. From there, you click on the PHP manager. Then, once you're on the PHP manager page, click on 'Register new PHP version'. Provide it with a path to the PHP executable file. That file is in the PHP folder that we created on our C drive. Click the three dots and navigate to your C drive. Then, click on the PHP folder and select the file named php-cgi.exe. Once you have given that file, click 'Okay'. You can double-check that you did it correctly by referring to the image above. You should see the duplicate content on your computer, as shown in the image in the PHP executable. Once you do that, close IIS and then reopen it. Then on the right-hand side, you should see stop and start buttons. Click Stop, wait for a few seconds, and then click Start to refresh IIS.  
</p>
<br />

<p>
<img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/42f99241-3172-4e02-b1ea-8a43e64f027a" />
</p>

<p>
From the osTicket Installation files, click on the osTicket v1.15.8 file. Right-click on the file and click 'Extract.' From here, set the destination as C:\inetpub\wwwroot and click 'Extract.' Once it's been extracted, go to the folder where you extracted it. Go to the C:\ drive, click on the inetpub folder, and then the wwwroot folder. Once you have extracted the file, you should see two folders. Upload and Scripts. Rename the upload file to osTicket.
</p>
<br />

<p>
<img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/df46ae44-9a12-4f28-abf2-b0ccf25d59c1" />  <img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/bb2aa47f-155c-402d-afd8-0727c84bde3b" />  <img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/ed876dae-06d3-4734-b421-75bd3c4dbd0b" />
</p>

<p>
The top image above shows IIS open once again as admin. Once you open it, the first thing to do is click 'Stop' and then start reloading it again. Then on the left-hand side, you should see sites. Click on that, and then you should see Default. Click on that until you see a folder called osTicket. Click on osTicket, then on the right-hand side, you should see something called browser 80 show up. Click on that, and it should open a webpage that resembles the image in the middle. You can see that many things are not checked green. This is because we need to enable some extensions. Now, go back to IIS and click on PHP Manager. Scroll down until you see a section called 'Enable or Disable an Extension'. Click on that and enable the following extensions: php_imap.dll, php_intl.dll, php_opcache.dll. Once you have done that, you should go back to the webpage and refresh it. It should look like the image at the bottom—mostly everything is checked green, except for the last two. 
</p>
<br />

<p>
<img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/1779c103-5d9c-4ccd-b2a4-a2779439c55f" />  <img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/a71e18f4-f361-4ce5-819a-ac121a7301ae" /> <img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/cd5a7d9b-7ae7-474a-b9f2-ec4d6f4298f9" />
</p>

<p>
The top image shows navigating to the path C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php and then, inside the include folder, looking for the file ost-sampleconfig.php. Change that to ost-config.php as shown in the middle image. Then, right-click on that file, click Properties, and then go to Security and click Advanced. Once you are there, disable inheritance. Once that is done, click the 'Add' button, then click 'Principles'. Once you are in that tab, type 'everyone' in the text box and click 'Check Names.' After that, click 'OK.' Check the box for everything in basic permissions. After that, your screen should look similar to the image at the bottom. Click 'Apply', 'OK', and then close everything. 
</p>
<br />

<p>
<img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/63a76671-0e8f-414c-9da1-17dba2b2bf60" />  <img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/84c78e7f-08c0-4b3e-868f-8e01c284a2bb" /> <img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/2ba87a5a-9814-4979-b561-4e7fdc7602b8" />
</p>

<p>
For this step, check the image at the top, then return to this website. At the bottom of the page, you will see a 'Continue' button; click that. Then, you will be taken to a page that resembles the image at the bottom. Please fill it out with your information. 
</p>
<br />

<p>
<img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/854c0a32-46fd-4657-aeaf-dd8e4eb8131f" /> <img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/8c03b634-4838-4439-ae10-4ebc4b8e7aed" />
</p>

<p>
From the osTicket Installation folder, click on the SQL file and download it. Once you reach the end of the installation, you will arrive at a page similar to the one shown in the image at the top. Check the box labeled 'Launch Heidi' and complete the installation. Hedi should open after that; click "Skip," and you will be taken to a page like the one in the middle image. In the bottom left corner, create a new session and fill in the username and password as 'root'. Connect to the session. Once you are connected, create a new database called osTicket and click 'Okay' to create.
</p>
<br />

<p>
<img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/8b55d214-20af-4547-8a12-fb9cc832be0d" /> <img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/fd4605da-fb4e-49a5-b5bc-11197f1f7318" />  <img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/2c835825-b4f0-4318-8895-495b54720d89" />
</p>

<p>
Go back to the osTicket installer website and complete the rest of the process. Make sure you name the SQL database 'osTicket', and set the username and password to 'root'. Once you have done that, click install now. Once it is installed, you should be able to access the following websites. Copy these URLs and paste them; you should see the same content as the middle and bottom images. http://localhost/osTicket/scp/login.php and http://localhost/osTicket/ 
</p>
<br />








<h2>osTicket Configurations</h2>







<p>
<img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/b296c306-c9ad-4405-a2d8-4acffba4ae0d" />
</p>

<p>
The image above shows how to configure roles in osTicket. Make sure you are in the admin panel. You can check which panel you are in by looking at the top right corner. Go to Agents and then select Roles. Create a new role, fill out the information as shown in the image above. In the Permissions tab, ensure that you choose all permissions, as this role is a Supreme Admin Role. 
</p>
<br />

<p>
<img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/146c5229-87c0-4bc1-83f2-2a6760016f26" />
</p>

<p>
The image above shows how to configure departments in osTicket. Make sure you are in the admin panel. Go to agents and then select departments. Create a new department, fill out the information as shown in the image above.
</p>
<br />

<p>
<img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/34349f5e-1de6-4f3d-9a70-d0e1788c985c" />
</p>

<p>
The image above shows how to configure teams in osTicket. Make sure you are in the admin panel. Go to agents and then select teams. Create a new team, fill out the information as shown in the image above.
</p>
<br />

<p>
<img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/268ac79b-65d4-4fdc-a471-00e4cc250447" /> <img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/3792458d-69a0-4505-a42f-0ae45653445e" />
</p>

<p>
The image above shows how to configure agents in osTicket. Make sure you are in the admin panel. Go to agents and select agents. Create a new agent, fill out the information as shown in both images above. For the password, click on 'Set Password', uncheck the box, and then set the password that you will remember. Also, please uncheck the box that says 'Change password upon logging in'. Make sure both boxes are unchecked and save the password. Then go to the access tab and fill out the information as shown above. Repeat this process for another agent, Jane. Except for the access tab, set her primary department as SysAdmin and grant her supreme admin access. For Jane only, go to Teams and change the teams to online banking.
</p>
<br />

<p>
<img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/06ba7591-308e-4ca0-b07b-c8af4a58ef03" />
</p>

<p>
The image above shows how to configure users in osTicket. Make sure you are in the agent panel. To access the agent panel, click on 'Agent' in the top right corner of the screen. Once in the agent panel, click on 'Users' and then click 'Create New User'. Fill out the information as shown in the image above. 
</p>
<br />

<p>
<img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/12377a13-862e-4fb0-9cb2-4f16b2d94bdf" />
</p>
  
<p>
The image above shows how to configure SLA in osTicket. Make sure you are back in the admin panel. Once in the admin panel, click "Manage," then "SLA." Create a new SLA and fill out the information as shown in the image above. This is just for SLA-A. Once you create SLA-A, make SLA-B(4 hours 24/7) and SLA-C(8hours Mon-Fri 8 am-5 pm).
</p>
<br />

<p>
<img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/9035a8ce-c71b-4015-847b-9105412ac416" />
</p>

<p>
The image above shows how to configure Help Topics in osTicket. Make sure you are in the admin panel. Click "Manage" and then click on "Help Topics." Create a new help topic and then fill out the information as shown in the image above. This is just for one help topic. After you create this one, make three more. They are called Business Critical Outage, Equipment Request, and Password Reset. For the parent topics,  use the same content as above, except for ' Password Reset ', which should be 'Report Problem Access Issue.
</p>
<br />

