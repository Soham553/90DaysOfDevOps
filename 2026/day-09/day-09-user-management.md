# User Management

 - Linux is a multiuser platform.
 - As we know, many people can work on a single server. Where arises the need for user management.
 - Operation team, developer, and many other roles.
 - Here is the need for isolation; one can not change the other, it works like that.


 # Types Of User

    1. Root user(Super User): One with full privileges.
    2. Regular user: A user who logs into the system.
    3. Service user: Created by the OS or services(Eg. mysql, nginx, systemd-network, daemon)


# /etc/userInfo
   - Linux stores user data in files inside /etc
   - /etc/passwd: stores username, password, UID, GID, and shell.
   - /etc/shadow: Contains encrypted passwords.
   - /etc/group: Store group information

 # Basic Commands for Creating and Deleting a User
    
     - sudo useradd username: it will create a user, but not create a home directory automatically
     - sudo useradd -m soham: It will create a user with a home directory.
     - sudo passwd username: It will redirect to enter the password for the username you will enter. Linux stores encrypted passwords in /etc/shadow.
     - su username: To switch from a user. 
     - sudo userdel soham: delete user
     - sudo userdel -r soham: Remove home directory also.
     - groupadd
     - gpasswd
     - usermod
     - sudo chown: to change Owner

 # User ID(UID)
     - Each user has a unique number
     - id user_name: Kernel uses UID internally.

# Groups 
     - Group simplify permission management.
     - sudo groupadd developers
     - Adding user to group:
          - sudo usermod -aG developers soham

# File Ownership
      - Every file has:
           1. Owner
           2. Group
           3. Others
      - If we do ls -l
           - -rw-r--r-- 1 soham developers file.txt
              - '-': Indicates file
              - 'rw-': Owner permission bit owner can read, write, but can't execute.
              - 'r--': Group permission bit, group can read only.
              - 'r--': Same for other users as group users.
# Locking and Unlocking Accounts
        - sudo usermod -L soham: Lock user
        - sudo usermod -U soham: Unlock user
        
 
    
            




















          
     
 
