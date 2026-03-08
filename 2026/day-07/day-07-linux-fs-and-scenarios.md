# File System Hierarchy In Linux

  - As we have heard many times, "Everything in Linux is either a file or a directory."
  - Linux file system hierarchy starts from the '/' directory.
  - All other directories are mounted in the '/' directory.
      ![Diagram](https://github.com/Soham553/90DaysOfDevOps/blob/master/2026/day-07/image.png)

  - We will start one by one

  1. /bin:

        - permission bits for /bin are: lrwxrwxrwx, which points to /bin -> usr/bin
          
        - It contains all the essential user commands.
    
  3. /boot:
         - permission bits for /boot are: drwxr-xr-x, which is a directory.

         - It contains Files and folders related to the Boot process.
     
         - efi, grub

  5. /dev:
         - permission bits for /dev are: drwxr-xr-x, directory.
     
         - It contains devices like character devices and block devices.

  7. /etc:
         - It contains .conf files for different services.
     
         - Manages all the OS functionality from networking to shutdown.
     
         - Eg. lvm.conf.

  9. /home:
         - It contains all the non-root users.

  10. /lib:
         - permission bits for /lib are: lrwxrwxrwx, which is sysmbolic link lib -> usr/lib
           
         - It contains shared libraries and kernel modules.

  11. /media:
          - Contains removable Media devices
      
          - External devices are mounted in the /media directory.
     
  13. /mnt:
          - Act as a mounting point for the other file systems
      
          - Eg. Physical Volume

 15. /opt:
          - Used to install third party application which are not included by default in the OS.
     
          - Eg, Google, Spotify.

 17. /proc:
          - It is like a virtual file system
     
          - It is like a live tracking system for Kernel.

 19. /root:
           - Home director for super user.
     
           - Permission bits for /root are: drwx------, which is a directory
     
           - Accessible by Owner.

21. /sbin:
           - SystemBinaries.
    
           - Contains binary executables, used by system administrators.
    
           - For system maintenace purpose.
    
           - Eg. iptables, reboot, fdisk, ifconfig.
