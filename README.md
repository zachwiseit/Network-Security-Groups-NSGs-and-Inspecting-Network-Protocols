<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)
- Windows App(macOS)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04
- macOS Sonama 14.6.1

<h2>High-Level Steps</h2>

- Create a Linux VM and a Windows VM
- Observe ICMP Traffic
- Configure a Firewall
- Observe SSH, DHCP, DNS, and RDP Traffic

<h2>Actions and Observations</h2>

Log into Azure and go to Resource Groups. 
<p>
<img <img width="1440" alt="ACN_2" src="https://github.com/user-attachments/assets/7c4c3741-07ca-481f-86df-8f758318b919" />
</p>
<p>
Click "Create".
<p> 
<img <img width="1440" alt="ACN_3" src="https://github.com/user-attachments/assets/79cb82ce-6c74-4858-8d37-000d5c8e5690" />
</p>
<p>
Choose a name for your Resource group. Then choose a Region
Click "Reviw + create".
<p> 
<img <img width="1440" alt="ACN_4" src="https://github.com/user-attachments/assets/dafa6038-85f8-46a4-83c5-b6e7536b3ffb" />
</p>
<p>
Click "Create".
<p>
<img <img width="1440" alt="ACN_5" src="https://github.com/user-attachments/assets/dd13c7dd-343c-4b43-aad5-24a171710042" />
</p>
<p>
After the resource group is built we will make the first virtual machine. 
<p>
<img <img width="1440" alt="ACN_7" src="https://github.com/user-attachments/assets/fe27f401-6ac3-492d-892b-44d286eabe9e" />
</p>
<p>
Go to Virtual Machines. Then click "Create". 
<p>
<img <img width="1440" alt="ACN_9" src="https://github.com/user-attachments/assets/ec9055a6-dcb0-4b80-8cb3-c15ef631e1e9" />
</p>
<p>
Choose the the resource group created earlier and the same Region as that resource group. 
<p>
<img <img width="1440" alt="ACN_10" src="https://github.com/user-attachments/assets/d3d22d5d-14f2-4a81-892e-986c7c5138a5" />
</p>
<p>
Scroll down, for the Image choose Windows 10 Pro, and for the size pick anything "with at least 2 vCPUs". 
<p>
<img <img width="1440" alt="ACN_11" src="https://github.com/user-attachments/assets/69b9be87-5df1-4cc8-baa9-dc27c4b7ef71" />
</p>
<p>
Scroll down, Choose a username, and password. 
Check the licensing box and click "Next : Disk". 
<p>
<img <img width="1440" alt="ACN_12" src="https://github.com/user-attachments/assets/2b5854b3-0f0b-4fc9-8321-e4010fbe85e8" />
</p>
<p>
Click "Next : Networking".
<p>
<img <img width="1440" alt="ACN_13" src="https://github.com/user-attachments/assets/279242cb-cda4-47cf-a169-6e261d14e4dd" />
</p>
<p>
Here we are going to create our own Virtual Network. (Normally this automatically created but this time we are making our own.)
To the right of Virtual network click "Create new".
<p>
<img <img width="1440" alt="ACN_16" src="https://github.com/user-attachments/assets/e26dfb86-f0a7-4249-a977-462205c4f271" />
</p>
<p>
Choose a name and then click "OK".
<p>
<img <img width="1440" alt="ACN_17" src="https://github.com/user-attachments/assets/286a0b99-0962-4ccb-825e-11861f543773" />
</p>
<p>
Leave everything else as is and click "Review + create". 
<p>
<img <img width="1440" alt="ACN_18" src="https://github.com/user-attachments/assets/eaca95d7-cabf-4268-811b-f385ccd2093b" />
</p>
<p>
Click "Create". 
<p>
<img <img width="1440" alt="ACN_19" src="https://github.com/user-attachments/assets/e9799a86-ab30-46a9-8731-77d06423d391" />
</p>
<p>
Now that it is complete we are going to create another Virtual Machine. 
<p>
<img <img width="1440" alt="ACN_22" src="https://github.com/user-attachments/assets/8f797673-3183-40b0-835c-756a5fa1b7ad" />
</p>
<p>
In VM click "Create" again. 
<p>
<img <img width="1440" alt="ACN_23" src="https://github.com/user-attachments/assets/6b4f66ec-1beb-4446-8544-cc3b5b90ba30" />
</p>
<p>
Choose the Resource group created earlier. 
For the VM name, choose something like "Linux-vm" or any name to help identify that this is a Linux VM. 
Choose the same Region as before. 
<p>
<img <img width="1440" alt="ACN_24" src="https://github.com/user-attachments/assets/4f735588-4b51-4a0a-a57a-620480583e31" />
</p>
<p>
Scroll down.
Image: choose UBuntu Server 22.04.
Size: Anything with at least 2 vCPUs.
<p>
<img <img width="1440" alt="ACN_25" src="https://github.com/user-attachments/assets/12610ff2-1adb-4223-8732-0351f0f6125a" />
</p>
<p>
Scroll down. 
Check Password and choose a username and password. 
Click "Next : Disk".
<p>
<img <img width="1440" alt="ACN_26" src="https://github.com/user-attachments/assets/1dd204b8-e5fe-4c1c-9eb9-bb7ee24c29fe" />
</p>
<p>
Click "Next : Networking". 
<p>
<img <img width="1440" alt="ACN_28" src="https://github.com/user-attachments/assets/16aefb9d-b46b-4632-bdb4-eaf93cff3eb9" />
</p>
<p>
For Virtual network choose the Vnet created earlier. 
Click "Reveiw + create".
<p>
<img <img width="1440" alt="ACN_29" src="https://github.com/user-attachments/assets/d81cbe52-266e-46aa-86c4-0bc7477da193" />
</p>
<p>
Click "Create".
<p>
<img <img width="1440" alt="ACN_30" src="https://github.com/user-attachments/assets/de766627-d11f-487f-bae1-08113e3a552c" />
</p>
<p>
With that our Linux VM is created. 
<p>
<img <img width="1440" alt="ACN_32" src="https://github.com/user-attachments/assets/cf78de25-1109-4de2-96cd-4762aafae966" />
</p>
<p>
Now we need to confirm that both VMs are on the same network. 
Go to Virtual Machines and click the linux vm.
<p>
<img <img width="1440" alt="ACN_33" src="https://github.com/user-attachments/assets/1b793641-22e6-4ce3-a69f-ee72ce278134" />
</p>
<p>
In Overview scroll down to Virtual network/subnet. 
The virtual network should be the one that was created and the subnet default. 
<p>
<img <img width="1440" alt="ACN_34" src="https://github.com/user-attachments/assets/f34995c7-b206-42a8-b91f-3645cab738b7" />
</p>
<p>
Do the same for the Windows VM and make sure it matches the linux VM. 
<p>
<img <img width="1440" alt="ACN_35" src="https://github.com/user-attachments/assets/3cbdd19f-5017-4f60-b816-e75163be1eca" />
</p>
<p>
I'm doing this from a macbook so I need to download and use the Microsoft Remote Desktop app to access these virtual machines. 
First go into Virtual Machines and copy the public IP address for the Windows VM. 
<p>
<img <img width="1440" alt="ACN_37" src="https://github.com/user-attachments/assets/a4cef65a-4820-409c-b67c-330138a62c33" />
</p>
<p>
Go back to the microsoft app and in the top right click "Add PC". 
<p>
<img <img width="1440" alt="ACN_38" src="https://github.com/user-attachments/assets/a0db48ff-0f61-4a3e-bc67-c9e0c6ed5fcd" />
</p>
<p>
Paste the public IP address in PC name.
Choose a Friendly name. 
Click "Add".
<p>
<img <img width="1440" alt="ACN_39" src="https://github.com/user-attachments/assets/714c4afc-d546-40bf-82a6-c4415ff81e7f" />
</p>
<p>
Now that the Windows VM has been added click on it. 
<p>
<img <img width="1440" alt="ACN_41" src="https://github.com/user-attachments/assets/e6cfbebb-69f0-4d80-9721-7483ea1d524d" />
</p>
<p>
Enter the credentials made earlier to sign into the Windows VM. 
Click "Continue".
<p>
<img <img width="1440" alt="ACN_43" src="https://github.com/user-attachments/assets/c8b9fef7-684d-4d6b-abfa-0e98e63e1c22" />
</p>
<p>
Click "Continue".
<p>
<img <img width="1440" alt="ACN_44" src="https://github.com/user-attachments/assets/786aedbc-b8ba-4c55-8381-23e3875314f8" />
</p>
<p>
Check no for all of these (they don't matter) and click "Accept".
<p>
<img <img width="1440" alt="ACN_46" src="https://github.com/user-attachments/assets/add6ed94-3996-44b4-84a6-b91afd8999f2" />
</p>
<p>
Next we need to install a protocol analyzer called Wireshark. 
From the home page open up Microsoft Edge and go to this link link https://www.wireshark.org/. 
<p>
<img <img width="1440" alt="ACN_47" src="https://github.com/user-attachments/assets/b1c45af4-ced6-4eb1-a704-ab5547a2971e" />
</p>
<p>
Now download the Windows x64 Installer 
<p>
<img <img width="1440" alt="ACN_50" src="https://github.com/user-attachments/assets/d974ec18-861e-453c-b505-343982a899e0" />
</p>
<p>
When it is finished downloading open the file in downloads. 
<p>
<img <img width="1440" alt="ACN_51" src="https://github.com/user-attachments/assets/80697e72-29ae-43fb-aed1-cd2b1358525a" />
</p>
<p>
On the set up page click "next". 
<p>
<img <img width="1440" alt="ACN_52" src="https://github.com/user-attachments/assets/f1189ef0-29ba-4783-abca-0d6399198cd6" />
</p>
<p>
Click "Noted". 
<p>
<img <img width="1440" alt="ACN_53" src="https://github.com/user-attachments/assets/70fff573-4e24-472a-82b3-bf7d1f34fda9" />
</p>
<p>
Click "Next".
<p>
<img <img width="1440" alt="ACN_54" src="https://github.com/user-attachments/assets/e2cc8519-9ec6-44fc-a288-20df9ba0c58c" />
</p>
<p>
Click "Next".
<p>
<img <img width="1440" alt="ACN_55" src="https://github.com/user-attachments/assets/1f344563-a8d9-4e8c-8e76-7d15f5d7009a" />
</p>
<p>
Click "Next".
<p>
<img <img width="1440" alt="ACN_56" src="https://github.com/user-attachments/assets/38e6f56a-dd25-4558-bccb-9b0a674b9a5f" />
</p>
<p>
Click "Next".
<p>
<img <img width="1440" alt="ACN_57" src="https://github.com/user-attachments/assets/b9c2f8d4-9f07-48b0-943c-f54b0744b8e6" />
</p>
<p>
Check the box for Install Npcap and Click "Next".
<p>
<img <img width="1440" alt="ACN_58" src="https://github.com/user-attachments/assets/7ce8ead3-8855-4d0e-97f6-5964ea29b285" />
</p>
<p>
USBcap isn't necessary. Click "Install".
<p>
<img <img width="1440" alt="ACN_59" src="https://github.com/user-attachments/assets/5d76b691-7e6f-4953-b4e5-8b52fb044b49" />
</p>
<p>
Wait for the installation to complete. 
<p>
<img <img width="1440" alt="ACN_60" src="https://github.com/user-attachments/assets/5378c3b9-829f-4718-91b6-30f46ba0415d" />
</p>
<p>
Click "I Agree".
<p>
<img <img width="1440" alt="ACN_61" src="https://github.com/user-attachments/assets/808b3524-5795-49b4-a153-57ffe4df1e69" />
</p>
<p>
Click "Install". 
<p>
<img <img width="1440" alt="ACN_62" src="https://github.com/user-attachments/assets/5d8b6cff-9fc0-43c8-be74-6432ffa6696a" />
</p>
<p>
When that is complete click "Next". 
<p>
<img <img width="1440" alt="ACN_63" src="https://github.com/user-attachments/assets/80ac5862-a61d-47c2-90f0-4bd2c0e662a6" />
</p>
<p>
Click "Finish".
<p>
<img <img width="1440" alt="ACN_64" src="https://github.com/user-attachments/assets/2ceaeae0-41ff-421a-b91b-9347ef06a8dc" />
</p>
<p>
Click "Next". 
<p>
<img <img width="1440" alt="ACN_65" src="https://github.com/user-attachments/assets/c5add192-3d50-47b1-b1b2-4dac2eb16f75" />
</p>
<p>
Click "Finish"  
With Wireshark installed we will be able to see the traffic between going to and from our Virtual machines. 
<p>
<img <img width="1440" alt="ACN_66" src="https://github.com/user-attachments/assets/3622f977-d579-4b5b-8e6b-3235b9cabc20" />
</p>
<p>
Now we are going open Wireshark and start a capture. 
Search for Wireshark in the search bar and open it. 
<p>
<img <img width="1440" alt="ACN_67" src="https://github.com/user-attachments/assets/0bba4378-3bb3-4470-8f7e-c1bee73be62a" />
</p>
<p>
Click on "Ethernet" you can see a little line forming. 
Indicating that Wireshark is seeing some network adapter. 
<p>
<img <img width="1440" alt="ACN_68" src="https://github.com/user-attachments/assets/c1a3a627-591a-4cbf-a407-0aaf1bf48038" />
</p>
<p>
Make sure Ethernet is Highlighted (by clicking on it). 
Then click the shark fin in the top left corner to Start capturing packets. 
<p>
<img <img width="1440" alt="ACN_69" src="https://github.com/user-attachments/assets/9dab7b31-b72b-46b2-8879-8584d6cbb27f" />
</p>
<p>
Now (in purple) you are seeing all the network traffic that is happening on the back end of this computer. 
<p>
<img <img width="1440" alt="ACN_70" src="https://github.com/user-attachments/assets/e26ebbd6-8064-439f-a2a6-dbffbc5a0dcf" />
</p>
<p>
Now we are going to filter for icmp traffic (Showing whenever something is pinged ). 
At the top search bar type icmp and enter. 
<p>
<img <img width="1440" alt="ACN_71" src="https://github.com/user-attachments/assets/805f82de-d391-433a-b345-68ef5f6d1115" />
</p>
<p>
Next we need to retrieve the private IP address of the linux-VM and attempt to ping it from within the Windows 10 VM. 
Back in azure go to Virtual machines and click the linux-vm. 
<p>
<img <img width="1440" alt="ACN_72" src="https://github.com/user-attachments/assets/9e96c173-38b7-43d8-bee5-4a87a30143b1" />
</p>
<p>
In Overview scroll down to Private IP address and copy that address. 
<p>
<img <img width="1440" alt="ACN_73" src="https://github.com/user-attachments/assets/646c5268-ca60-4f79-bc0e-103b1230331b" />
</p>
<p>
Now go back into the Windows VM and open up Powershell. 
<p>
<img <img width="1440" alt="ACN_74" src="https://github.com/user-attachments/assets/7bafff74-e75a-4956-b0fe-f454f2198e25" />
</p>
<p>
From here we are going to attempt to ping the Linux VM from the Windows VM
<p>
<img <img width="1440" alt="ACN_75" src="https://github.com/user-attachments/assets/8c71d513-935b-4693-a072-173237710433" />
</p>
<p>
Type ping followed by the private IP address of the Linux VM and press enter. 
<p>
<img <img width="1440" alt="ACN_76" src="https://github.com/user-attachments/assets/e26b373f-7ed7-485a-a5fa-5d856a524b29" />
</p>
<p>
You will get a few replies from the Linux VM. 
<p>
<img <img width="1440" alt="ACN_77" src="https://github.com/user-attachments/assets/276db2ed-5e74-41a0-99e6-218c3c0bd05e" />
</p>
<p>
Here is the icmp traffic in Wireshark with the filter. 
<p>
<img <img width="1440" alt="ACN_80" src="https://github.com/user-attachments/assets/261e4b7f-117f-486f-a2e9-461f0ef133dd" />
</p>
<p>
Now we are going to clear this and restart the capture. 
In the top left click the green shark fin to Restart current capture. 
<p>
<img <img width="1440" alt="ACN_81" src="https://github.com/user-attachments/assets/6a57f506-df4e-436f-8c69-e8cc25fbb974" />
</p>
<p>
Click "Continue without saving".
<p>
<img <img width="1440" alt="ACN_82" src="https://github.com/user-attachments/assets/224e0e1f-2f38-4d4b-9be7-1bd7e41afede" />
</p>
<p>
In Powershell do that same ping again. 
<p>
<img <img width="1440" alt="ACN_83" src="https://github.com/user-attachments/assets/1959b108-e451-4cf3-a0d1-7ff5d493fd89" />
</p>
<p>
In powershell you can only see the four replies. 
<p>
<img <img width="1440" alt="ACN_84" src="https://github.com/user-attachments/assets/8be852ba-41a4-4a52-afe4-9469ddd0c773" />
</p>
<p>
With the filter you can see both the request made by the Windows computer and the reply from the Linux Computer. 
<p>
<img <img width="1440" alt="ACN_86" src="https://github.com/user-attachments/assets/c2cbbe47-02f4-4dc9-b7c2-dc353a36cd5a" />
</p>
<p>
If you click on the first capture you can see a lot of information in the bottom left box. 
<p>
<img <img width="1440" alt="ACN_89" src="https://github.com/user-attachments/assets/e15dac2f-75c3-47f3-a49a-a7afbab940f7" />
</p>
<p>
Expand Ethernet II and that will show you the mac address and the source mac address. 
<p>
<img <img width="1440" alt="ACN_90" src="https://github.com/user-attachments/assets/4b321fd6-f444-43f3-897a-d7d8687196ea" />
</p>
<p>
Go back into Powershell and type "ipconfig /all" and press enter. 
<p>
<img <img width="1440" alt="ACN_91" src="https://github.com/user-attachments/assets/39cbb2fa-0a73-4d23-9454-8d95ac0184b2" />
</p>
<p>
Here you can also see the physical Address. 
<p>
<img <img width="1440" alt="ACN_92" src="https://github.com/user-attachments/assets/689f0312-6b66-4a3a-a2e4-d23bc6d8b89d" />
</p>
<p>
Going back to Wireshark you can see the same Physical Address.
<p>
<img <img width="1440" alt="ACN_93" src="https://github.com/user-attachments/assets/95ea1f22-d1ae-423b-a762-9d808dfb001d" />
</p>
<p>
Collapse Ethernet two and expand Internet Protocol showing the network layer. 
Here you can see information like the source IP address (Windows VM private IP address). 
<p>
<img <img width="1440" alt="ACN_95" src="https://github.com/user-attachments/assets/5b858b58-d471-4fbd-9519-6cc569502ef7" />
</p>
<p>
Back in ipconfig you can see that address there as well. 
<p>
<img <img width="1440" alt="ACN_96" src="https://github.com/user-attachments/assets/e8484d67-bb66-414b-94db-37019c013bee" />
</p>
<p>
Now collapse Internet Protocol and expand the ICMP (Internet Control Message Protocol). 
<p>
<img <img width="1440" alt="ACN_97" src="https://github.com/user-attachments/assets/ff94b629-e189-40fc-af45-931b2ad4879b" />
</p>
<p>
Here you can see the Data Payload (the data actually sent in the ping). 
<p>
<img <img width="1440" alt="ACN_98" src="https://github.com/user-attachments/assets/6350a7ce-06b9-4fae-bf52-1211d3b75141" />
</p>
<p>
Now ping is just a connection test but with this you can actually see the data that was sent in the ping. 
<p>
<img <img width="1440" alt="ACN_99" src="https://github.com/user-attachments/assets/cb76dbad-cf24-4f1e-b03c-20967ddf577a" />
</p>
<p>
If you click on the next packet you will find very similar information except reversed. 
<p>
<img <img width="1440" alt="ACN_100" src="https://github.com/user-attachments/assets/305bf1e4-fb24-4e63-b2a3-8a480c615738" />
</p>
<p>

  Use this link to move on to the next steps in the tutorial. [Configuring-Firewalls-and-Monitoring-Common-Network-Protocols](https://github.com/zachwiseit/Configuring-Firewalls-and-Monitoring-Common-Network-Protocols/blob/main/README.md)
