# steps-to-install-centos7
this repository is design to install centos7 with GUI

Step 1: Download the latest version of centos from the below link and make your pendrive bootable.

        http://isoredirect.centos.org/centos/7/isos/x86_64/CentOS-7-x86_64-Minimal-1708.iso
         
         If you dont have linux usb creator download from here:
         https://www.pendrivelinux.com/yumi-multiboot-usb-creator/

step 2: Insert your pendrive and start your computer and boot pendrive after pressing your boot button like F12/F9/F8/F10 whaterver 
        acceptable for your system. now select centos to install.
        
        
Step 3: Now centos window will come and choose your drive where you want to install centos:
        there are two options to install centos in your machine -
         1. Automatic Partition.
         2. In a specific partition of your machice.
         
         1. If want to automatic partition for installing centos in this process it will create a automatic new partition in
         Hard Disk in will install centos on this partition.
         
         2. If you want to install centos on a specific partiotion than choose that partition and press (-) minus button . It will 
          clear that amount of memory in unused memory and that partition will disapper but dont worry its auto selected now just click on (+)
          button and create some required partitions which are as follows-
            --> / (its root partition for OS give size in GB, like 50 GB)
            --> /home (its home partition for OS give size in GB, like 50 GB)
            --> /swap (its for swaping if RAM is not enough to complete the process than computer use this partition as a RAM 
                 give size in GB, like 8 GB)
            --> /bootable (its optional partition sometimes its required somtimes not, first try without this if its asking then give 
                 size in Mb like 500 Mb)
        
        Now memory allocation complete click on "Done" button in left upper corner of the screen and now click on "Install" button.
  
  Step 4 : Now let it complete to install create user and root password during installation . after installation it will ask reboot , 
           give reboot and now black window will come login here.Username "root" and Password is that what you given during installation
           if not given leave password blank and press enter.I hope that you login successfully to your root user.
  
  step 5 : Now install GUI to centos.
  
  step 6 : Check internet is connected or not on your computer using below command:
  
            nmcli d
            
  step 7 : Connect internet on your computer using below command:
            
            nmtui
  
  step 8 : Enable ONBOOT = yes
           
           goto network-scripts folder using this command:
           cd /etc/network-scripts
           
           and edit anyone file out of these
           ifcfg-enp1s0/ifcfg-enp0s3 these files are different for every system find your one
           
  step 9: Install GNOME Graphical User Interface using below command:
  
           yum -y group install "GNOME Desktop" "Graphical Administrative Tools"
          
  step 10: Check default UI mode its Graphical or Command line using below command :
  
           systemctl get-default
            
  step 11: set default target "GNOME UI" on load of operating system using below command
            
           systemctl set-default graphical.target
            
            
            
        ************* installation complete hope it will help you for installing centos *************    
            
  
