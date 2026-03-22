# Linux Architecture, Processes, and "systemd."

   * The Linux-Based OS's Architecture:
        - We all know the onion analogy, we peel off each layer and give each layer as a Linux component.
          
            Layer-1. Operating System: the first layer, which provides a user-friendly interface to communicate with the kernel.
          
            Layer-2. Shell/Scripting: the interface to communicate with the kernel effectively.
          
            Layer-3. Kernel: an intermediate program between hardware and software. Indirectly, the kernel is an interface to communicate with the hardware.
          
            Layer-4. Hardware

                 ![Linux Architecture](https://github.com/Soham553/90DaysOfDevOps/blob/master/2026/day-02/Linuxarec.webp)

   * Processes:
        - A process in Linux is nothing but a running command, application, or any other program.
          
        - There is a famous statement on Linux-based OS:
          
                    "Everything in Linux is either a file or a process."
    
        - For example, whenever we run a command, it is considered a process.
    
        - Command to check the running processes:

                 ps: displays all the current running processes in the shell

        - The first process to start after boot is systemd, having PID:1.
    

  * Systemd:

       - systemd is the init process that replaces the old sysvinit process. It is the first process that runs having PID:1 and PPID:0.
   
       - systemd is the init process as well as the service manager for the modern Linux-based systems.
   
       - systemd can run many processes at a time.
   
       - systemctl is a tool to communicate with systemd.
   
       - journald it is systemd's daemon, it is a logging system which stores messages from services and applications in a structured manner.
   
       - journalctl is a tool to communicate with journald.
   
       - Unit files at the core of systemd store all the information in the form of unit files.
   
       - Unit files are how systemd knows what to do.
   
       - Unit files:
                1. services
                2. Target Units (.target)
                3. Socket Units (.socket)
                4. Mount Units (.mount)
                5. Timer Units (.timer)

      - We can create our own unit file.
   

* Basic commands of systemd and journald

         # Managing Services with systemctl

             1. Listing services
  
                  - systemctl list-units-type=service: shows all services currently loaded.

             2. Starting, stopping, and restarting services

                  - systemctl start <service>: launches a service immediately.
                  - systemctl stop <service>: stops a running service.
                  - systemctl restart <service>: completely stops and then starts a service again.
                  - systemctl reload <service>: tells a service to reload its configuration files without fully stopping.

             3. Enabling and Disabling Services at Boot

                  - systemctl enable <service>: configures a service to start automatically at boot time.
                  - systemclt disable <service>: prevents a service from starting automatically when the system boots
                  - systemctl enable — now <service>: enables the service for future boots while also starting it immediately.

             4. Checking Service Status
  
                  - systemctl status <service>: shows detailed information about a service, if it’s running, when it was started, recent log entries, and more.
                  - systemctl is-active <service>: returns “active” if the service is running or “inactive” if it’s not.
                  - systemctl is-enabled <service>: tells you whether a service is configured to start at boot.

             5. Reloading systemd Configuration

                  - systemctl daemon-reload: tells systemd to reread all unit files. You must run this after creating or modifying unit files for systemd to recognize


        # Creating Logs with Jornalctl

             1.  Viewing Logs by Services
  
                  - journalctl -u <service>: shows logs from a specific service.
                  - journalctl -u <service> -f: shows you a live stream of the log entries as they are generated.
                  - journalctl -u <service1> -u <service2> : shows logs from multiple services at once. 

       












