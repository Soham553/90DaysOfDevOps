Run and record output for at least 6 commands
Include 2 process commands (ps, top, pgrep, etc.)
Include 2 service commands (systemctl status, systemctl list-units, etc.)
Include 2 log commands (journalctl -u <service>, tail -n 50, etc.)


Process Commands:
1. ps:  Displays a static snapshot of currently running processes.
   ps aux
   USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
  root           1  0.0  1.4  22236 13352 ?        Ss   17:28   0:01 /sbin/ini
  root           2  0.0  0.0      0     0 ?        S    17:28   0:00 [kthreadd

2. ps -ef: Process relationship focus.
   UID          PID    PPID  C STIME TTY          TIME CMD
  root           1       0  0 17:28 ?        00:00:01 /sbin/init
  root           2       0  0 17:28 ?        00:00:00 [kthreadd]

3. top: The  top  program  provides  a  dynamic real-time view of a running
       system.
4. htop:pcp-htop - interactive process viewer.

Service Commands:

systemctl - Control the systemd system and service manager

1. systemctl start Process_Name: Use to start particular process.
2. systemctl status Pricess_Name: Use to see wheather process is active or not.
   ● nginx.service - A high performance web server and a reverse proxy server
     Loaded: loaded (/usr/lib/systemd/system/nginx.service; enabled; preset>
     Active: active (running) since Fri 2026-02-27 17:28:10 UTC; 1h 19min a>
       Docs: man:nginx(8)
    Process: 527 ExecStartPre=/usr/sbin/nginx -t -q -g daemon on; master_pr>
    Process: 576 ExecStart=/usr/sbin/nginx -g daemon on; master_process on;>
    Main PID: 597 (nginx)
      Tasks: 3 (limit: 1015)
     Memory: 3.7M (peak: 4.0M)
        CPU: 35ms
     CGroup: /system.slice/nginx.service
             ├─ 597 "nginx: master process /usr/sbin/nginx -g daemon on; ma>
             ├─ 599 "nginx: worker process"
             └─1135 "nginx: worker process"
  
   Feb 27 17:28:10 ip-172-31-38-27 systemd[1]: Starting nginx.service - A high>
   Feb 27 17:28:10 ip-172-31-38-27 systemd[1]: Started nginx.service - A high >
   
 3.systemctl is-active: If the process is active it will return active.
 4. systemctl list-units:  List units that systemd currently has in memory.
     UNIT                                                                     >
      proc-sys-fs-binfmt_misc.automount                                        >
      sys-devices-pci0000:00-0000:00:04.0-nvme-nvme0-nvme0n1-nvme0n1p1.device  >
      sys-devices-pci0000:00-0000:00:04.0-nvme-nvme0-nvme0n1-nvme0n1p14.device >
      sys-devices-pci0000:00-0000:00:04.0-nvme-nvme0-nvme0n1-nvme0n1p15.device >
      sys-devices-pci0000:00-0000:00:04.0-nvme-nvme0-nvme0n1-nvme0n1p16.device >
      sys-devices-pci0000:00-0000:00:04.0-nvme-nvme0-nvme0n1.device            >
      sys-devices-pci0000:00-0000:00:05.0-net-ens5.device                      >
      sys-devices-platform-serial8250-serial8250:0-serial8250:0.1-tty-ttyS1.dev>
      sys-devices-platform-serial8250-serial8250:0-serial8250:0.2-tty-ttyS2.dev>
      sys-devices-platform-serial8250-serial8250:0-serial8250:0.3-tty-ttyS3.dev>
      sys-devices-pnp0-00:04-00:04:0-00:04:0.0-tty-ttyS0.device                

 5. systemctl list-automounts:  List automount units currently in memory, ordered by mount
           path.
    WHAT        WHERE                    MOUNTED IDLE TIMEOUT UNIT             >
    binfmt_misc /proc/sys/fs/binfmt_misc yes     -            proc-sys-fs-binfm>
    
    1 automounts listed.
    
6. systemctl list-paths: List path units currently in memory, ordered by path.
    PATH                      CONDITION         UNIT                           >
  /etc/acpi/events          DirectoryNotEmpty acpid.path                     >
  /run/systemd/ask-password DirectoryNotEmpty systemd-ask-password-console.pa>
  /run/systemd/ask-password DirectoryNotEmpty systemd-ask-password-wall.path >
  
  3 paths listed.
   
