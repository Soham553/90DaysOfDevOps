# File Ownership

   - the user who creates the file, who automatically becomes its initial owner
   - We can see the file group and owner using the command:

           - ls -l

   - To change the ownership and group of the file:

           - chown new_owner file_name: It will change the owner
           - chgrp
     
   - To create a new group:
     
            - sudo groupadd group_name.
            - sudo usermod -aG group_name username: To add a user to a group.
