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

- We can connect to the instance using the shell in Windows. Bash is best
- While connecting to the server using SSH, the private key should be in the current working directory
- As we know, while creating an instance, we have created a key pair.
- A public and a private key. Public key is alwayes in the server, and private key should be in the machine through which we are connecting.
- .pem is the format of a private key file
- Befor inserting connection string we have to change the permission bits of .pem file
- chmod 400 ".pem file"
- Now enter the connection string.
- connection string:  ssh -i "Name_of_server"Public_DNS
    
   
