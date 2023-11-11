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

</p>
