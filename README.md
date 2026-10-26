SETTING UP CYBERSECURITY LAB
BANGO-B083-WK1-PM1
Cybersecurity Lab Setup Using Kali Linux and VirtualBox
Objective: To prepare a basic cybersecurity lab environment by installing VirtualBox, configuring a virtual network, setting up Kali Linux, and creating a shared folder.
Step 1: Download and Install Oracle VirtualBox
Visit the official VirtualBox website at https://www.virtualbox.org/ and download the installer for the host operating system. Run the installer and follow the setup instructions to complete installation.
 
Step 2: Configure a NAT Network in VirtualBox
Open Oracle VirtualBox Manager and go to the Network settings. Create a NAT Network named “NatNetwork,” set the IPv4 prefix to 10.0.0.0/24, and enable DHCP. Save the configuration.
 
Step 3: Download Kali Linux
Visit https://www.kali.org/get-kali/ and select the pre-built virtual machine option for VirtualBox. Download the Kali Linux virtual machine image suitable for VirtualBox.
 
Step 4: Import Kali Linux into VirtualBox
Extract the downloaded virtual machine archive if needed. In VirtualBox Manager, add or import the Kali Linux virtual machine by selecting its .vbox configuration file, then finish the import process.
 
Step 5: Start and Test Kali Linux
Start the Kali Linux virtual machine and sign in. If the default credentials have not been changed, the pre-built image may use the username “kali” and password “kali.” Check that the desktop loads correctly.
 
Step 6: Configure the Network Connection in Kali Linux
Open the virtual machine settings and select Network. Under Adapter 1, enable the network adapter, set “Attached to” to “NAT Network,” and choose “NatNetwork.” Make sure “Cable Connected” is checked, then click OK. In Kali Linux, check the network menu for “Wired connection 1.” You can verify the interface with the terminal command `ip a` and test internet connectivity with `ping -c 4 google.com`.
Note: Kali Linux normally appears to use a virtual wired connection in VirtualBox even when the host computer is connected to Wi-Fi.
 
 
Figure 1. Kali Linux virtual machine network adapter set to NAT Network.
Step 7: Create a Shared Folder
Open the virtual machine’s Settings and select Shared Folders. Click the add-folder icon and choose the folder on the Windows host that you want to share. In this setup, the selected path is `C:\Users\ITCU\Desktop\Kali Linux`. Set access to Full and enable Auto Mount, then click OK to save.
After saving, verify that the shared folder is accessible from Kali Linux. This setup helps transfer files between the host computer and the virtual machine.
 
Figure 2. Shared folder configured in the Kali Linux virtual machine settings.
What I Learned
In this laboratory activity, I learned how to set up a cybersecurity lab environment using Kali Linux and Oracle VirtualBox. I learned how to install and configure VirtualBox, create a NAT Network, and connect the Kali Linux virtual machine to the network. I also learned how to create a shared folder between my Windows host computer and Kali Linux to make file sharing easier. Through this activity, I gained a better understanding of virtualization, network configuration, and file sharing, which are important skills in cybersecurity. This hands-on experience helped me understand how to prepare a safe and organized environment for practicing cybersecurity tasks.
Conclusion
The lab setup provided a working starting point for cybersecurity practice. VirtualBox allows Kali Linux to run as a virtual machine, the NAT Network provides network connectivity, and the shared folder makes file exchange between the host and guest systems more convenient.
