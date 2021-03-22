## TASK 2.1 
### PART 1. HYPERVISORS
 1) The most popular hypervisors are VmWare, Oracle VM VirtualBox and Microsoft Hyper-V.
 2) As stated earlier, the most popular hypervisors are  VmWare, Oracle VM VirtualBox and Microsoft Hyper-V. 
VMware Workstation Pro is a 64-bit hosted type 2 hypervisor capable of implementing virtualization on Windows and Linux systems and has some features include host/guest file sharing, the creation and deployment of encrypted VMs, and VM snapshots.
VMware is type 1 hypervisor that includes the ESXi hypervisor and vCenter management software to provide a suite of virtualization products, such as the vSphere Client, vSphere software development kits, Storage vMotion, the Distributed Resource Scheduler and Fault Tolerance. VMware vSphere  geared toward enterprise data centers; smaller businesses might find it difficult to justify the price.
Oracle VM VirtualBox is type 2 an open source hosted hypervisor that runs on a host OS to support guest VMs. VirtualBox offers multigeneration branched snapshots, Guest Additions, guest multiprocessing, ACPI support and Preboot Execution Environment network boot.
Microsoft Hyper-V is type 1 hypervisor that runs on Windows OSes and enables admins to run multiple OSes inside a VM. Admins and developers often use Hyper-V to build test environments to run software on several OSes by creating VMs for each test.
### PART 2. WORK WITH VIRTUALBOX
During the process of completing this part of the task:
1) the main possibilities of VM control were studied, groups of VM's were created, several snapshots were made and VM .ova file was exported and then imported;
2) USB ports, shared folder and different network modes were configured; 
3) basic commands of VBoxManage list were executed.
#### Branch of snapshots:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m2/task2.1/Branch%20of%20snapshots.png)
#### Group of Vm's (VM1, Cloned VM and imported from .ova file VM):
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m2/task2.1/all%20VM's.png)
#### Configured USB connection:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m2/task2.1/Usb%20connection.png)
#### Added shared folder:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m2/task2.1/Adding%20shared%20folder.png)
#### Table of possible connections:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m2/task2.1/Table.png)
### ! To ensure ping of the host machine, Windows firewall was specially disabled !
#### Configured NAT network connection:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m2/task2.1/vm1-vm2%20IP%20and%20connection.png)
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m2/task2.1/Pinging%20host.png)
#### Configured Host-only network connection:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m2/task2.1/Host-only!!.png)
#### Configured Internal network connection:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m2/task2.1/Internal.png)
#### Configured Bridged network connection
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m2/task2.1/bridged.png)
#### Executed commands of VBoxManage list:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m2/task2.1/commands.png)
### PART 3. WORK WITH VAGRANT
During the process of completing this part of the task:
1) default Vagrant box was initialized and launched;
2) connection to the VM using PuTTY was configured;
3) Own Vagrant box and test environment from a few servers were created.
#### Default Vagrant box launching and PuTTY connection configuration: 
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m2/task2.1/vagrant/vagrant%20start.png)
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m2/task2.1/vagrant/putty.png)
#### Configured and launched my own Vagrant box
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m2/task2.1/vagrant/Launching%20my%20own%20vagrant%20box.png)
#### Configured and launched test environment:
#### Code of test environment you can check here [Test Environment](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m2/task2.1/vagrant/Test%20Environment)
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m2/task2.1/vagrant/testenviroment%20vagrant.png)



