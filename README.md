<p align="center">

  ![image](https://github.com/DsosaH/AzureBasics/assets/148100125/3f070720-1865-41e2-a61e-b398010aeb00)

</p>
<h1>Azure Basics: VMs, NSG and Network Protocols</h1>
In this presentation I'll show how the basics of Microsoft Azure work and can be utilized by analyzing common Internet Protocols such as ICMP, SSH, DHCP, etc.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Wireshark

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)
- Linux (Ubuntu)</br>

<h2>Setting up inside Azure</h2>
<p>
  First thing we need to do is create a <b>Resource Group</b>, these are storages inside of our Azure subscription that can be used to store any service we may need, like a <b>Virtual Machine</b> or a <b>Network Security Group</b>.<br>
  We can easily create one by going into the <b>Resource Group</b> tab and clicking on <b>Create Resource Group</b>.

  ![image](https://github.com/DsosaH/AzureBasics/assets/148100125/6032af21-02ec-49a0-9fb1-b858db1280a1)<br>
  
  Choose a Subscription and a Name, then create and you should have your group ready to use.
  
  ![image](https://github.com/DsosaH/AzureBasics/assets/148100125/f603e3bd-f2f8-4a1f-b81e-3f97baa25851)
</p>
<p>
  Now that the group is created, we can begin to put it into use. In this case We'll create a Virtual Machine (VM) and a Network Security Group (NSG).<br>
  To create a VM, just type Virtual Machine in the search bar and create.

  ![image](https://github.com/DsosaH/AzureBasics/assets/148100125/064e3f0f-a852-4101-86bd-749399a291fb)

  Inside the Virtual Machine creation settings first thing we need is to make sure we are using the correct Subscription and Resource Group.<br>
  Then, choose a name for the VM, a region and the desired OS.

  ![image](https://github.com/DsosaH/AzureBasics/assets/148100125/9e57fc28-d564-4e75-9680-2d4bec12cae4)

  Choose a size based on how powerful and fast do you need you VM to be, but remember that the better the more expensive it'll be.<br>
  Choose a username a password and note them down somewhere. Also make sure to agree to the license use.
  
  ![image](https://github.com/DsosaH/AzureBasics/assets/148100125/d92d2cc9-db90-419c-98d4-8b59731c54a5)

  We'll also create our NSG at the same time with our VM, for this go to the Networking tab and just make sure that the option indicates that a new NSG is being created, you  can modify the name and Subnet if necesary. Fina;;y just click create and wait until the VM and the NSG are created.

  ![image](https://github.com/DsosaH/AzureBasics/assets/148100125/10433741-d895-4094-b86f-a74cdee94a45)

  After the deployment is done, you can find your VM and NSG inside your resource group ready to use. 
  ![image](https://github.com/DsosaH/AzureBasics/assets/148100125/baebbb48-70ca-49a8-ad56-b7497b23c5c2)

</p>
<h2>Testing Internet Protocols (IPs)</h2>
<p>
  Now that we know how to deploy VM and NSG, We'll use Remote Desktop to get inside our virtual machine and test some Internet Protocols. For this, We'll need to create another VM so we can connect and see how the protocols work in real time.<br>
Following the same steps, We'll create a new VM, with the exception that this time we'll set the OS to Linux(Ubuntu) and select the already created SNG instead of creating a new one.

  ![image](https://github.com/DsosaH/AzureBasics/assets/148100125/d9e8871f-ce52-4159-bbda-84865df1678a)
  ![image](https://github.com/DsosaH/AzureBasics/assets/148100125/e1fc2fe8-429c-4582-9ec7-b3d30fa1bc4c)
  
  Next step is using Remote Desktop to connect to our Windows OS Virtual Machine. First, we need to get our VM's public IP, for this we simply go to the resource group our VM resides, click on it and search for the public IP. Copy the public IP.

  ![image](https://github.com/DsosaH/AzureBasics/assets/148100125/b959607a-05e4-4ebe-ac32-3c7c83a963e1)
  
  Open Remote Desktop app, enter the IP and then your previously created credentials. Now you should be able to connect to your Virtual Machine.<br>
  ![image](https://github.com/DsosaH/AzureBasics/assets/148100125/4ba322d9-77be-4dcb-aed2-86d2fb5e7f48)
  ![image](https://github.com/DsosaH/AzureBasics/assets/148100125/1d5c3bbf-ef47-42f8-99b7-0e8b66e21c1b)
</p><br/>
<p>
  Now, inside our VM, We'll download and install WireShark, a software that will help Us understand how IPs function.<br>
  After installing the software, open and select the ethernet connection. In the window that opens will appear all our IPs that are happening at any giving moment.<br>
  
  ![image](https://github.com/DsosaH/AzureBasics/assets/148100125/fa97cc6c-5c15-47af-ac2f-6207facbcc51)

  The IPs here are not filtered, so they can seem a little erratic, but luckily we can filter them out to watch only the ones that are of our interest. In this case, We'll filter by ICMP (Internet Control Message Protocol), which is the protocol used for reporting 
  errors and performing network diagnostics. Very useful as a starting point when solving a problem.<br>
  First, we write ICMP in the upper bar for the filter to work. Now the screen should be white for no protocol has been activated yet.<br>
  ![image](https://github.com/DsosaH/AzureBasics/assets/148100125/da259f85-9571-4b52-a07a-5863f8410911)

</p>


