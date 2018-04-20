
VirtualBox is a powerful x86 and AMD64/Intel64 virtualization product for enterprise as well as home use. Not only is VirtualBox an extremely feature rich, high performance product for enterprise customers, it is also the only professional solution that is freely available as Open Source Software under the terms of the GNU General Public License (GPL) version 2. See "About VirtualBox" for an introduction.

Presently, VirtualBox runs on Windows, Linux, Macintosh, and Solaris hosts and supports a large number of guest operating systems including but not limited to Windows (NT 4.0, 2000, XP, Server 2003, Vista, Windows 7, Windows 8, Windows 10), DOS/Windows 3.x, Linux (2.4, 2.6, 3.x and 4.x), Solaris and OpenSolaris, OS/2, and OpenBSD.

VirtualBox is being actively developed with frequent releases and has an ever growing list of features, supported guest operating systems and platforms it runs on. VirtualBox is a community effort backed by a dedicated company: everyone is encouraged to contribute while Oracle ensures the product always meets professional quality criteria. Advantages
1) Multiple Operating Systems at a time without restarting the single computer.

2) Completely isolated virtual environment from host OS. Therefore no risk involved in virus, malware or any kind of threat spreading from guest to host machines, except thorough network or USB flash drive transfer.


 
3) You can run your old legacy applications and Operating systems on your latest computer. Let’s say you bought a latest Windows 7 laptop recently and now you like to run your old important legacy application which will not work on Windows 7. Here comes virtualization software… Just setup a Windows XP or older versions of OS by VMware/VirtualBox/Virtual PC then install your legacy application and use it.

4) Snapshot Feature, which helps to restore the virtual machine back and forth to a specific date/time. For example, today you can take snapshot of a virtual machine and if tomorrow something goes wrong with that particular virtual machine, do not worry, you can restore the virtual machine to previous day’s state by snapshot feature.       10 ways to get the most from VirtualBox                     1: Use virtual appliances

Virtual appliances allow you to quickly spin up a full-blown server with a specific use in mind. These appliances range from production-ready CMS tools to groupware servers, calendars, shopping carts, and everything in between. A number of sites are dedicated to virtual appliances, my favorite being TurnKey Linux. These virtual appliances allow you to have a complex system up and running in no time.

2: Set networking to Bridged mode
This one catches a lot of users. When you set up a new virtual machine, the networking will automatically be set to NAT. This means the resources on your network won't be able to see the device. To resolve this issue, you have to set the networking to Bridged mode. Unfortunately, you can't set up VirtualBox to automatically default to Bridged mode for every virtual machine, so you have to set every VM manually. To do this, go to the virtual machine's Settings | Networking | Attached To and select Bridged Adapter from the drop-down.

3: Don't skimp on RAM
This should be a no-brainer, but I find more and more people attempting to run virtual machines with limited resources. Think of it this way: You want to have enough RAM on the host to hand over to the guest so that 1) the host has enough RAM left over to function and 2) the guest has enough RAM to function properly. This is the case for every guest you create. For a simple example, if you have an Ubuntu Linux host running three Windows 7 virtual machines, you'll want to have 16 GB of RAM on the host machine. Of course, this assumes all three guests will run simultaneously. If the guests are Windows 7, that's unlikely. But if you're running multiple servers on the host, you'll need to have plenty of RAM to hand out to each server.

4: Use snapshots
A snapshot is the best way to roll back a virtual machine to a previous state. If you're not using snapshots you are missing out on one of the best features of virtual machines. Using snapshots means that if something goes horribly awry, you can simply roll back to a previous running state and be good to go. (Just avoid what you did to cause you to have to roll back.) To create a snapshot, click on the Machine menu (while the machine is running) and select Take Snapshot. You'll be prompted to enter a name and description for the specific snapshot and then you can click OK to save it.

5: Get to know the commands
VirtualBox has a number of built-in commands that can help you manage your virtual machines and much more. The main command is VBoxManage, which can handle such tasks as importing/exporting virtual machines, starting virtual machines, attaching storage, cloning hard drives, and configuring virtual machines. These commands can get fairly complex, so you'll need to give yourself plenty of time to go through the commands and command structure. For more information about the command, take a look at the VirtualBox manual, chapter 8.

6: Watch for guest clock drift
If you've found the time on your guests constantly drifting, you might have to fix that from the command line. This is done like so:

 VBoxManage guestproperty set "<vm_name>" "/VirtualBox/GuestAdd/VBoxService/—timesync-set-threshold" 1000

where vm_name is the name of the virtual machine you need to alter.

7: Use phpVirtualBox
If you want to be able to manage your virtual machines from the network, you can install phpVirtualBox. With this AJAX take on the VirtualBox user interface, you can access and control your VirtualBox virtual machines. phpVirtualBox was designed to allow a headless deployment of VirtualBox.

8: Install vboxadditions
Anyone using a virtual host should always install the additions. This is true with VMware and VirtualBox. The add-ons have to be installed on a per-machine basis and are done post operating system install. The add-ons include device drivers and system applications to help optimize the guest/host experience. You'll enjoy better mouse integration, better video support, shared folders, seamless windows, and improved host/guest communication.

9: Reclaim space by compressing images
If you've allocated a specific amount of space for a virtual machine and it's nearing that limit, you can compress the image with the command:

VboxManage modifyhd "path_to_target_image.vdi" compact

where path_to_target_image.vdi is the path and filename of the virtual machine. Before you run that command, you'll want to remove unused data (such as temp files), defrag the drive, and then use something like CCleaner's drive wipe. Shut down the image and then run the command.

10: Clone virtual disks
If you've created virtual machines that you want to use for other purposes, don't bother re-creating them — clone them! Cloning makes an exact copy of the virtual machine so you don't have to go through the steps of reinstalling and reconfiguring the guest platform. To clone a virtual machine, select it and then click Machine | Clone. You can create either a full clone or a linked clone. If you plan on moving the clone, be sure to create a full clone; otherwise, the moved clone will not work.
