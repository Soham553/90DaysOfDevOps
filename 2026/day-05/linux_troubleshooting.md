Run and record output for at least 8 commands (save snippets in your runbook)
    - Environment basics (2): uname -a, lsb_release -a (or cat /etc/os-release)
    - Filesystem sanity (2): create a throwaway folder and file, e.g., mkdir /tmp/runbook-demo, cp /etc/hosts /tmp/runbook-demo/hosts-copy && ls -l /tmp/runbook-demo
    - CPU / Memory (2): top/htop/ps -o pid,pcpu,pmem, comm -p <pid>, free -h, vm_stat (mac).
    - Disk / IO (2): df -h, du -sh /var/log, iostat/vmstat/dstat.
    - Network (2): ss -tulpn/netstat -tulpn, curl -I <service-endpoint>/ping.
    - Logs (2): journalctl -u <service> -n 50, tail -n 50 /var/log/<file>.log.

# Environment Basics:

1. uname -a: It prints the system information, including the kernel, network node hostname, and hardware, etc. Also about OS.
       - The order in which the output is printed is:
             1. Kernel Name(-s)
             2. Current IP address(-n)
             3. Version of Linux Kernel(-v)
             4. machine hardware name(-m)
             5. Processor Type(-p)
             6. Hardware Platform(-i)
             7. Operating System(-o)
   
   - All the above info I got from the command uname.

2. lsb_release: print distribution-specific information
       - LSB stands for Linux Standred Base
       - It is standred set to ensure compatibility of Os
       - Early, when distros were being built, they were not run on other distros
       - we we cmd it, it will give info about:
           Distributor Id, Release, Codename

# File System Sanity

1. fsck: File System Condition Check
    - Use on unmounted partitions
    - When the file system becomes inconsistent, this cmd use to repair it.
    - The file system has an internal structure, superblock, inode table, Block bitmap, directory tree, and journal
    - fsck actually checks the above structure to find inconsistencies.
  
2. dumpe2fs: Use to display information about the primary and backup superblocks on the partition. 
     - sudo dumpe2fs /dev/sda1 | grep -i superblock
     - it returns the Group Descriptor Table(GDT)

3. tune2fs: adjust tunable file system parameters on ext2/ext3/ext4 file systems
           
