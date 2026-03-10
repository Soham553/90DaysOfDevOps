# File Permissions & File Operation

  - File Creation and writing in a file commands

          - touch file_name: create file
          - vim file_name: To open a file in the editor. (If the file is present, it will open in the editor; if not, it will be created.
          - ls -l file_name: To check the file permission bits and owner.
          - cat file_name: To print the content of the file in the current window.
          - head -n: Prints the first n lines of the file.
          - tail -n: Prints the last n lines of the file. 

  - What are permission bits?
         ![image](https://github.com/Soham553/90DaysOfDevOps/blob/master/2026/day-10/image.png)

       - -rw-rw-r-- 1 ubuntu ubuntu 31 Mar  8 07:30 Notes.txt
          1. '-': Represents a file
          2. 'rw-': Owner's permissions bit. The owner can read and write, but can't execute a file.
          3. 'rw-': Group's permissions bit. The group users can read and write, but can't execute a file.
          4. 'r--': Other users can only read the file.
             
      - We can change the permission bits of a particular directory or a file using the chmod cmd.
   
                      Octal Value 	Binary Representation	    Symbolic Representation	         Description
                          7	              111                          rwx               	Read, write, and execute
                          6	              110	                         rw-	                   Read and write
                          5	              101                          r-x	                  Read and execute
                          4	              100	                         r--	                      Read only
                          3              	011	                         -wx	                    Write and execute
                          2	              010	                         -w-	                       Write only
                          1              	001	                         --x	                      Execute only
                          0	              000	                         ---	                      No permissions
        
       - chmod 400 Note.txt
       - Then permission bits become:
              - For owner: r--
              - For Group: ---
              - For others: ---


             

      
