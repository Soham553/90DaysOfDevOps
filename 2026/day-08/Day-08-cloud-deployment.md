# Creating an Instance At AWS

   Step 1: Name and tags
   
      - Give the name, for instance
   Step 2: OS Image
   
      - As per your choice, the OS for your server.
   Step 3: Instance type
   
      - It determines the hardware of the host computer.
      - Each instance type offers different compute, memory, and storage capabilities.
   Step 4: Key Pair 
   
      - Create a key pair that is used to connect server through ssh
      - It creates two keys: one is a private key, and the other is a public key.
  Step 5: Network settings
  
      - Create a security group
      - Allow ssh traffic from anywhere
  Step 6: Configure storage
  
      - As per your usage
  Step 7: Launch the instance.

# Connecting instance through SSH
   ![image](https://github.com/Soham553/90DaysOfDevOps/blob/master/2026/day-08/Screenshot%202026-03-08%20180945.png)

- We can connect to the instance using the shell in Windows. Bash is best
- While connecting to the server using SSH, the private key should be in the current working directory
- As we know, while creating an instance, we have created a key pair.
- A public and a private key. Public key is alwayes in the server, and private key should be in the machine through which we are connecting.
- .pem is the format of a private key file
- Before inserting the connection string, we have to change the permission bits of the .pem file
- chmod 400 ".pem file"
- Now enter the connection string.
- connection string:  ssh -i "Name_of_server" Public_DNS

# Starting A Service
   ![image](https://github.com/Soham553/90DaysOfDevOps/blob/master/2026/day-08/Screenshot%202026-03-08%20180945.png)

   - Nginx
      - It is the process that we are going to start.
      - Linux based os system have systemd, which acts as a  service manager.
      - We can access systemd using systemctl, which is like a tool, through which we can cmd to systemd.
      - Command to start nginx:
            - ~# systemctl start nginx

   - Inbound:
      - It is a kind of set of rules that allows incoming traffic or requests to the server
      - Suppose, if we allow an HTTP request to the server, it will use PORT 80

           ![image](https://github.com/Soham553/90DaysOfDevOps/blob/master/2026/day-08/Screenshot%202026-03-09%20143630%20-%20Copy.png)

     - After editing the inbound rule, we can visit it using the IPv4 of our instance on PORT 80

       ![image](https://github.com/Soham553/90DaysOfDevOps/blob/master/2026/day-08/Screenshot%202026-03-09%20142010%20-%20Copy.png)
    
   
