# Azure-Honeypot

<h2>Description</h2>

In this lab, I created a Honeypot in Azure using the T-Pot Honeypot Framework inside a Virtual Machine.</b>

<h2>Virtual Machine</h2>

To begin this lab, first an Azure account needs to be created for the VM. You get $200 credits for free when you first sign up. For students, you get $100 credits with no credit card needed and 12 months of free Azure services. </b>

When an account is created, look for the "Virtual Machine" tab or search it in the search bar
to be taken to this page, click on "Create" to start the process of making the VM.</b>

<center>
<img width="1127" alt="Screenshot 2024-03-18 152705" src="https://github.com/horeacio/Azure-Honeypot/assets/100793672/f50cd994-caa7-4dce-93a6-753bb56bbe57">
</center>

As you start the process, you'll need to make a resource group for the VM since it's a resource. Name the resource group "tpot-rg" and the resource "tpot-vm". Fill in the following details to match the screenshots. Make sure you know the password you're using. Once done, move on to "Disks".</b>

<center> 
  <img width='1127' alt="Screenshot 2024-03-18 153613" src="https://github.com/horeacio/Azure-Honeypot/assets/100793672/198b859f-3ec3-4268-825c-2b4d18799319">
  <img width='1127' alt='Screenshot 2024-03-18 153819' src='https://github.com/horeacio/Azure-Honeypot/assets/100793672/9c14f9c7-bd91-4c38-993a-0dd92b596e2f'>
</center>

Under "Disks" change the disk size to "128 GiB (P10)"</b>

<center> 
  <img width='1127' alt='Screenshot 2024-03-18 154014' src='https://github.com/horeacio/Azure-Honeypot/assets/100793672/849e5e78-72ba-4907-bc19-33f0f1f45389'>
</center>

Under "Networking" check the box "Delete public IP and NIC when VM is deleted".</b>

<center>
  <img width='1127' alt='Screenshot 2024-03-18 154155' src='https://github.com/horeacio/Azure-Honeypot/assets/100793672/d00584cc-e51f-4883-a133-236ec1fa418e'>
</center>

Go to "Management" and click on "Create" to finish the process. </b>

<center>
  <img width='1127' alt='Screenshot 2024-03-18 154406' src='https://github.com/horeacio/Azure-Honeypot/assets/100793672/cca54b42-48c7-4f26-951e-c9fdf83afbd6'>
  <img width='1127' alt='Screenshot 2024-03-18 154522' src='https://github.com/horeacio/Azure-Honeypot/assets/100793672/f4a98c37-2d5b-48b6-b0e9-d64cb5b9eee5'>
</center>

Now that the VM is created, we need to change the inboud security rules for the Honeypot. Click on the VM and look for the "Settings" tab and click on "Inbound Security Rules". Click on "Add" and change the port ranges to all "*" and the priority to 100. </b>

<center>
  <img width='1127' alt='Screenshot 2024-03-18 154649' src='https://github.com/horeacio/Azure-Honeypot/assets/100793672/443d85fb-0193-42aa-9cdb-827e44c0cf4b'>
  <img width='1127' alt='Screenshot 2024-03-18 15480' src='https://github.com/horeacio/Azure-Honeypot/assets/100793672/f622fba9-da43-425f-959c-b6170eb50f7d'>
</center>

We made our VM vulnerable, next we need to grab the IP address. You can find it under the "Overview" when you click on the VM. 172.174.232.184 is our IP address.</b>
<center>
  <img width='1127' alt='Screenshot 2024-03-18 155857' src='https://github.com/horeacio/Azure-Honeypot/assets/100793672/8d26047f-9679-45e6-9fc4-ff3300bddaee'>
</center>

<h2>Installing T-Pot Framework</h2>
