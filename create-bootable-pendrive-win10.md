# Easy steps to create a bootable Pen drive using Windows 10
A bootable Pen drive is mainly required to install Operating System from a downloaded ISO file. Creating a bootable Pen drive using Windows is very easy. There is no requirement for other third-party software. You required to know a few CMD commands to make your bootable Pen drive. These are the simple steps for making your bootable Pen drive with CMD.
1. *Open CMD as administrator:* Type CMD in the search bar, right-click and select run as administrator.  Click yes. Now CMD will open. Type the following commands in order.
2. *diskpart:* Diskpart is a command-line disk partition utility available with Windows. This command opens the Diskpart utility in your CMD. Now the address changed to DISKPART.
3. *list disk:* It lists all the disks available on your PC, including the Pen drive.
4. *select disk <Number> :*  It will select the disk. Change the number according to your Pen drive. In my case, it is 2. So I used select Disk 2.
5.*clean:* This command will clear all the configuration information and all the information on your disk.
6. *create primary partition:* This will create a new partition in your Pen drive.
7. *select partition 1:* This command used to select the newly created partition.
8. *active:* This mark the selected partition as active.
9. *format fs=ntfs quick:* This will format the disk in NTFS.
10. *assign:* This will assign a mount point to the selected partition.
11. *exit:* Exit from the diskpart utility.
12. Copy the content of the ISO files to your Pen drive.
Done!
