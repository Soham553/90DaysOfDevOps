# User Management

 - Linux is a multiuser platform.
 - As we know, many people can work on a single server. Where arises the need for user management.
 - Operation team, developer, and many other roles.
 - Here is the need for isolation; one can not change the other, it works like that.


 # Types Of User

    1. Root user(Super User).
    2. Regular user.
    3. Service user.

 # Basic Commands for Creating and Deleting a User
    
     - sudo useradd username: it will create a user in the '/home' directory.
     - sudo passwd username: It will redirect to enter the password for the username you will enter.
     - su username: To switch from a user.
     - cat /etc/group: contains all the information related to groups.
     - groupadd
     - gpasswd
     - usermod
     
 
