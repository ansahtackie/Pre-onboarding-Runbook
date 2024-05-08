![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/7554630d-1507-4048-b7f8-c912b9478828)![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/dbd3a032-2d01-47f9-9760-5c0b94fc03e6)# Pre-onboarding-Runbook

## Objective

The goal of this career simulation was to use the knowledge of Windows operating system and management techniques to solve a problem and write a runbook to document the findings. The deliverable for this project involved demonstration of understadning of asset and invetory management, system administration, computer languages,interpersonal skills, problem solving, and writing. 


### Skills Learned

- Joining a computer to a given domain.
- Switching from a computer to a server, creating a user for a new hire, and setting a password.
- Creating a group with a given department name and placing the user in the group.
- Creating a share on the server with the department name and share it only with the people who belong to that deparmtnet (read and write permissions).
- Creating a text document in a given folder.
- Creating an Organization Unit (OU) with the department's name and placing the user, group, and computer in the OU and attaching a Group Policy Object (GPO) to the OU created.
- Editing a GPO and applying given set of rules.
- Checking the Event Viewer on the server machine and writing down the last successful login from the user.
- Using PowerShell to check the latest program installed on a computer.
- Writing a PowerShell script that gives a list of all running services and putting that in a named file.
- Writing a runbook documenting the processes for setting up a machine for new hires.


### Tools Used

- Windows machine
- PowerShell for scripting.


## Steps
  

#### Step 1: Join the computer to the domain (the domain name is contoso.com)

- Longon to your computer, go to the search bar and type “control panel.” This will bring a pop-up window with the “control panel” option. Click on “control panel.”

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/f4936bbe-83f9-4d42-af51-2b9e5646aba8)

- Click on “control panel.” This will open the “control panel” window shown below.


 ![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/88991388-56f0-4f71-a29b-dbf6ca879340)



- Click on “Network and Internet”


 ![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/c9ec2adc-ee9a-4abb-abbb-2a70dc62c36a)


- In the “Network and Internet” window, click on “Network and Sharing Center” to open the “Network and Sharing Center” window.


 ![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/8ed1f3db-1dcf-4471-a73a-7b2d58fa0bbf)




- In the Network and Sharing window, on the left-hand side, click on “Change Adapter Setting”
  

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/df978b62-7d24-40ec-a94b-136420ea20d4)




- When you click on Change Adapter Setting, a new window with the heading name “Network Connections” will pop up. 

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/099fada0-3bf9-4c94-94e0-dfd58d5450e5)


- Right-click on the “Ethernet 2” icon and click on “Properties.”

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/3ed38bc2-da3b-4804-a68f-41f1a7cb7331)




- On the “Ethernet 2 Properties” window, double click Internet Protocol Version 4 (TCP/IPv4)

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/c9d45f41-0eba-4833-9b6e-b53b5f4857a5)




- On the Internet Protocol Version 4 (TCP/IPv4) Properties window, scroll down and select “Use the following DNS server address.”  In the spot that says “Preferred DNS server,” you will get the IP address of the server and paste it here. Before leaving this window, click “OK”


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/1a5f59c5-f84b-4b94-a2ea-8053e1a8fcc6)




- Now, the computer is ready to receive the IP address of the server. Open the server and type CMD (for command prompt) in the search bar. This will open a window with the “Command Prompt” option. 


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/69a36336-edf7-4bc9-bd77-870ccf588f0f)



- Click on the “Command Prompt” to open the “Terminal”


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/310f3e86-e5d9-43c0-878c-b16d876ffda7)




- Type “ipconfig” in the terminal and click “Enter” or “Return” to run the “ipconfig” command. Select the IPv4 Address and copy only the IP Address of the server. For this example, the IP Address of the server was 172.31.10.184


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/fef5bf56-19d1-4efd-993e-33816b6cbdc8)



- Note that the IP Address of the server can be obtained directly from the server. To get the IP Address from the server, look at the top right corner of the server. 

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/70ec87b2-aa50-465b-bc6d-c551cc7fec84)




- On the computer, put the IP Address of the server in the spot that says “Preferred DNS server”. Then click “OK” to get out of this window.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/7eaac16d-b603-4154-8346-33db0c446968)



- Once the IP Address has been entered on the computer as the “Preferred DNS server”, you can connect the computer to the server. To do so, go back to “Control Panel” by clicking on “Control Panel.” 

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/13a41d9a-a761-44d7-9171-80a35248f13f)



- On the “Control Panel” window, click on “System and Security” Click on Control panel and go to “System and security.”

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/c3424f7d-951b-4ff4-8b2d-c32f0f554c88)



- In the “System and Security” window, click on “System”. This will open a new window called “Settings.”
  ![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/d5a9bdb6-4f09-4928-9bdd-1828398f2045)


- In the “Settings” window, click on “Advanced system settings” which is located at the extreme right hand side of the page. “Advanced system settings” is located under the heading “Related settings.”  Once you click on “Advanced system settings,” a new window, “System Properties,” will pop up. 


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/ecef311a-716c-4c3d-bb58-df9c202c52a0)




- In this window, click on “Computer Name.” You can find “Computer Name” at the top left on the “System Properties” window. After clicking on “Computer Name,” you will see the name of the computer you are trying to join to the server and the Domain name. For this example, the name of the computer is “Desktop-2 contoso.com and the Domain is “contoso.com.” Then click on “Change”

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/91a7d4bf-abe8-4c7c-b47b-2aa133a5400d)



- After clicking on “Change”, a new window called Computer Name/Domain Changes will pop up. On this pop up you should see the name of the computer you are trying to join to the server (Desktop-2 for this example). For the Domain, section in the window, you should go to the serve to get the name of the Domain and paste it in this space.

  ![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/d2a7141c-f06e-455f-bb0d-79051355a3a2)




- On the server, type “Server Manager” in the search bar. This will open up a window window with the “Server Manager” option. Click on the “Server Manager.”


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/58fe3750-0f87-4df6-8631-0dda49c892ed)



- After clicking on the “Server Manager” a new winder called “Server Manager Dashboard” will open.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/86ae48e6-924b-43ec-b991-dbe1ba3297cf)




- Click on “Local Server.” Check the name of the Domain you want to connect the computer to. For this example, the Domain name is “contoso.com.” Also, check to see that the server name is correct. 


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/b386ed21-f5cc-47eb-a423-a577b2ac2d17)



- Then go back to the computer you are trying to join to the server. This should have the following window. Type the name of the Domain (contoso.com) in the Domain space shown in the window aobve. Then click “OK.”

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/f37c73b2-7a45-41e4-b0c2-74f81e86f111)




- After clicking “OK,” there will be a “Windows Security” pop-up window that asks for a username and password of an account with permission to join the domain. Enter the username and the password. For this example, the username was “administrator” and the password was “Pa$$w0rd”


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/644b9178-f74d-471a-bc1a-9c1a94da95d7)


- The final entry should hide the password. Click “OK.” 

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/b56a7a1f-d3a4-4e79-89a9-a4b7919c1ac6)


- After clicking “OK” a new window will appear with the word, “Welcome to contoso.com”. Click “OK” on this new pop-up window.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/4c284ae5-4b19-400b-909f-4297a3b3d8ef)



- When you click “OK” a new window should pop up with the message, “You must restart your computer to apply these changes”. Click “OK” and then restart the computer.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/3c539a34-df8a-46f3-b4f1-be6a352202a3)








#### Step 2: Switch to the server, create a user for the new hire and set a password

- On the server machine, type “Active Directory Users and Computers”. This should open a window showing “Active Directory Users and Computers”. Click on “Active Directory Users and Computers”.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/96dedbc1-a44d-4c11-9123-246908fc67f1)



- In the “Active Directory Users and Computers” window, click on “contoso.com” from the left column. Select “Users” 


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/48745fb9-ef17-4186-9b37-f3b044df9ff6)




- Right-click on “Users”. This will open a list of options. Click on “New.” When you click on “New,” another list with different options will open. Click on “User” to create a new “User”. 


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/5dbd02f8-9543-4e77-96ee-2e3b552f91d5)



- When you click on “User”,  the “New Object-User” window will open. Fill the credentials for the user. In the New Object-User window, enter user information by providing the first name, last name, full name, user logon name. Then click “Next”.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/7a886347-b01f-4d55-b8bb-b2f019b68813)



- After clicking “Next” a new window will open. This window will ask for a password and a confirmation of the password. Enter a password for the new user you have created and confirm the password. Then click “Next”. 


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/62b4edfa-b2c4-4e1c-9dba-74104c5f23dd)



- After clicking “Next” the next window should show the information of the new user. Click on “Finish”.
  

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/89b15d59-7c9e-479f-9b47-ba194b6f8c0d)



- Back in the Active Directory Users and Computers, click the arrow in front of “contoso.com” to drop down the folders. Scroll down to “Users” and click on it to display all the users. Check to see if the new user created is in the list. If the new user is in the list, that means adding the user has been successful. For this example, the user is “Emma Johnson”
  
![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/e3801663-5689-4039-827e-9f2213652c5d)







#### Step 3: Create a group with the department name and place the user in that group


- Still, in the Active Directory Users and Computers window, right-click in an empty space where the is the list of users. This will open a list of options. Select “New”. When you select “New” another list of options opens. Click on “Group”.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/3f5ffb7b-17f9-42c5-9924-e6a87f0f5b90)



- Click on “Group” to open a pop-up window called “New Object-Group”

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/9195e9dc-73c8-4642-9f50-a52d17a1d2d5)



- Enter the “Group name” in the first space. As you type the group name in the first space, the same name will populate in the second space. For this example, the group name was “Marketing”. Click “OK”.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/f96a4a8c-64db-492d-8fb2-a5f28880b354)


- After clicking “OK” you should see the new group “Marketing” in the list of users.
  
![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/c65f5ce6-2f1b-4b17-bc85-ac12bb57a058)


- To add the user (Emma Johnson for this example) to the group (Marketing), right-click on the new user (Emma Johnson).  This gives opens up a list of options. 

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/2474bdd1-3455-4df9-acd8-06b90b666ea6)


- Select and click on “Add to group”.
  
![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/4be25287-54a5-4ca8-a223-890cc94eb5ec)



- In the next window, enter the name of the group you want to add the new user. In THIS example, the name of the group was “Marketing”. Type this name in the space.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/e341af29-6796-421c-9316-e671318387e3)


- After typing the name (Marketing), click on “Check Names” to be sure that the group (Marketing) exists. If the group exists, the name in the space will be underlined. Click “OK”.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/f4c2a47b-f456-4d5c-8013-1449a0d5ab36)



- In the final window, there will be a new pop -up window with the name “ Active Directory Domain Services” with the message, “The Add to Group operation was successfully completed” 


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/4ddfcc4a-2273-4ab8-aa1f-aa8654ebd706)






#### Step 4: Create a share on the server with the department name and share it only with people who belong to that department



- On the desktop of the server machine, click on the “File Explorer” icon next to the internet explorer icon.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/ca32df53-f7e7-4ebf-a169-9546c50c7f77)



- Click on Documents from the left side of the window. Select “New folder” from the top. 


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/a9a824ff-c749-4699-ad19-203390200d0d)




- Click on “New folder from the top. This will create a new folder. 

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/9ee94cde-df54-45c7-b1e3-1fba184b05c4)



Name the new folder to match the name of the group that was created. In this case, the name of the folder will be “Marketing”.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/08941752-7f3b-4fad-9747-57ff020e6474)


Create a new Text Document in the new folder. To do this, click on the drop-down arrow named “New Item” and click on “Text Document”.


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/d91a2ad8-48a8-4f4f-9a82-227b6da2a896)


In the next window, a new text document will be created. 

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/1df48b6a-e2d9-444c-9a16-cb6c55cac91b)




Name the text document. For this example, the name was “test.txt”


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/af4f9209-97da-471e-93e6-314f8927800b)



To share the new folder and the document with the correct department (in this example, Marketing), click on the “Share” tab from the top. Then click on “Specific people.”


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/fe9d35d2-f031-48fa-ad28-64f6f5492b20)



In the File Sharing window that opens, enter the name of the group in the space and click add. You can also search for the name.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/734a457e-2031-4153-8824-1a24375b1432)


Give the “Read and Write” permission to the department. To give this permission, select the department and click on the drop-down arrow to select the correct permission. Then click “Share”.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/1ad8a054-f03e-4f18-93cf-07d484517c0c)


In the next window you should see the message, “Your folder is shared”. Click on the “copy” link to copy the link for the shared folder. Click “Done”.


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/26c0a6e3-3c0a-4019-a8fe-111eb3f52f46)


On the computer (in this case Desktop 2), switch users from fstack to the new user (Emma Johnson). To do this, click on the start button located at the bottom left of the desktop. Click on “Switch User” to get a screen for “Other User”. Click on “Other User” from the bottom left corner. Enter the username and password for the new user.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/240aef29-ee34-4d19-afa4-af926048180d)




Click on the forward arrow to open to the new user. This might take some minutes. Do not turn off the computer at this point.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/1ea77dcc-5f37-4b8f-8075-b3933d450e94)



Click on the start icon located on the bottom left of the desktop.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/bc3dd79b-fdf0-47df-87d2-840c79433050)


In the search bar past the copied link in this bar. If the paste option does not work type the link to the shared folder in this bar. 


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/c6a4f759-ea9f-4e34-ba2b-3ed0876c84c5)




After typing or pasting the copied link, press “Enter”. This will take you to the shared document.


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/65e5d9ac-318b-4fcd-9cb9-7a0c2521fed1)



Test to see that the read and write permissions work. Open the text document and type in it. 

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/9a0de9ff-0b33-4c7a-8507-0b2adaf0db84)




#### Step 5: Create an OU with department name and place the user, group, and compiuter in the OU. Attach a GPO to the OU


On the server machine, enter “Active Directory Users and Computers” in the search bar. Click on Active Directory Users and Computers.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/39764ec8-78b2-44f9-903a-bb40139431b2)


In the Active Directory Users and Computers window, click on the arrow on contoso.com to drop down all the folders. Select Users from the list of folders.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/4cb5aaee-604b-4c17-94f3-9b004fd54725)


Right-click on the empty space in the right column to open a window with a list of options. Select “New”. Another window will open. Select “Organizational Unit”

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/accdaf14-3504-4962-96ee-28e2dc5b2c7b)



Enter the Organizational Unit name in the space provided in the window below.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/6829f325-9d6b-4922-9d75-9be4146cc09d)



Click “OK” to open up a new window. You should see the new Organizational Unit (OU) in the list of OUs created.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/e563ed21-09af-485c-abc9-f8cecaf47065)



To move the group that was created and the user into the OU, click and drag the group from the list of users into the OU created. When attempting to drop the dragged object into the OU, a pop-up window will appear with a warning. Read the warning before clicking on “Yes”!


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/90b4281b-c369-49dc-9ee3-4c68657afb36)


In the same manner, move the user to the OU. In this example, Emma Johnson was moved to the OU.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/5342ea03-7e0b-4835-a0d8-ff4567ce1bba)


Finally, move the computer into the OU. To get the computer, click on the OU named “Computers”. This opens a window with a computer. Drag the computer into the OU created.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/1409ddb1-e97c-43f5-98b4-c4e933cf10ec)



Click on the OU created (in this case Marketing) to check if the three objects (Desktop-2, the user, and the group) have been moved.


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/bb07a539-bf60-4fe9-b44c-86236509419d)


To attach the Group Policy Object (GPO), type Group Policy Object in the search bar. This will open a window with Group Policy Object, Click on it.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/79cd00ad-6301-48fc-ba6e-f5d8f499e3f8)


Select the Group Policy Object folder from the left-hand side. 


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/f0b618d4-e830-4cdb-8dcc-3e8b28fc671d)


Right-click on Group Policy Object and click on “New”

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/4964ddd9-0610-4808-92ed-278757d71291)



A new pop-up window called “New GPO” will open.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/ff43c687-d0a4-4277-9d75-efb7c9938f42)


Enter the name of the Group Policy Object (GPO). Click “OK”

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/e7e10df9-3b71-4609-8210-b964b60d0a27)


The new GPO is highlighted in blue. 

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/de204186-48a8-4bb2-a56a-7b3a8bcc071d)


Right-click on the Organizational Unit that was created (Marketing). Click on “Link an Existing GPO”. A pop-up window will appear asking if you want to link. Click “OK”

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/32ec884c-c874-42e7-a42a-eb5c01ac1dab)


Check the new window to see the GOP linked.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/863c6bab-0e81-49db-b88e-dcafd8b3659e)





#### Step 6: Edit the GPO and apply given rules:

##### *Applying rule 1: A message should appear whenever the computer starts (do not install unauthorized programs)*

In the group Policy Management, click on the departmental name. In this case, click “Marketing” to show the created GPO. Right-click on the GPO.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/20d0de6b-5b6c-42f4-993b-e4066445031d)


Click on “Edit”.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/dbf45184-65fd-4879-a8de-dbf703f14bce)


Click on Computer Access Control Policy. Under Computer Configuration, Click on Policies to drop down its folders.


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/0dbe639a-4544-4644-8431-490aba5f2890)


Click on Windows Settings to drop down its contents.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/bcf7b94b-0b35-4da9-8800-b256573c9194)



Click on Security Settings to drop down its contents.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/16af8bf8-525c-4b8c-82c8-043ab2e15f8c)


Click on Local policies to drop down its contents.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/c3eed9b8-5de6-4e25-b0ea-201b2fa60ec3)


Click on the Security Option. Select Interactive Logon: Message text for users attempting to logon Not Defined.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/342c458a-f398-4a4d-8e8d-d2d2c28ec8d3)



Double-click it to get the new window.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/05810915-add1-47c4-afc5-2ca20095ff73)


In the opening window check the box that says “Define this policy setting in the template” and type the rule, “do not install unauthorized programs”. Click “OK”.

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/0c087bc9-9a7c-4a7f-b136-12942402194a)


Click “Apply”  then “OK”

![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/42ccc3fc-0a5a-4b40-b0b9-b6d59b998fd0)




##### *Applying rule 2: Prevent the user's access to CMD*

On the same page, scroll down and get to User Configuration. Follow similar process to apply all the rules. The pictures to go with the steps are presented below. 


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/521d1760-0ed9-4ca4-a5c6-4aa326a22bfb)



![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/c0f79b99-593e-4c52-9e0f-82968f1e10f4)



![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/b385231b-315f-4559-93ef-7e88e3c29aaf)



![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/d7493149-3a8c-49b7-951e-fe1f3378189d)



![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/fc0e2271-5817-4dc1-bd1d-2b11cf97780f)


![image](https://github.com/ansahtackie/Pre-onboarding-Runbook/assets/148600552/c7089c5c-04d5-4bbf-bf9a-b7e05f61c528)





##### *Applying rule 3: Add script to the user's login to map the share you created*


To add the script, follow the same steps as described in the other rules. The following are pictures to help. 











##### *Applying rule 4: Disable the run command from the start menu*



















#### Step 7: Check the Event Viewer on the server machine and write down the last successful login




#### Step 8: Use PowerShell to check the latest program installed on the computer




#### Step 9: Write a PowerShell script that gives a list of all running services


## Selected Screenshots



