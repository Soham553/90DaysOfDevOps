cheat sheet of commands:

Process Management:  

1. systemctl start process_name: Use to start a service just by passing the name of the process.
2. systemctl stop: Use to stop an active process ( systemctl stop nginx).
3. systemctl is-active: 
4. systemctl is-failed 
6. systemctl status process_name: Show runtime information about the whole system or about one or more units
7. systemctl try-restart process_name
8. systemctl kill 
9. systemctl list-automounts: List automount units currently in memory.
10. systemctl list-sockets: List socket units currently in memory.
11. systemctl list-timers: List timer units currently in memory.

File System: 

1. touch File_Name: To create a new file.
2. mkdir Folder_Name: Creates folder.
3. mkdir -p josh/hell/files: Creates the folder as defined in the path, including the file.
4. vim/nano File_Name: Opens file in vim/nano editor.
5. cat File_Name: Opens file contents in read mode.

Networking troubleshooting:

1. ping google.com: Use to check host reachability using ICMP.
2. ip addr: Displays network interfaces and their configuration(IP, MAC address, MTU).
3. ss -ta: To list tcp connections
4. ip route: To see the exact route for a specific IP address.
5. di google.com ANY: To get common records.
6. nslookup: 
