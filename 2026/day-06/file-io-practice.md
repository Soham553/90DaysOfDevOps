
# Creating a new File
   - touch file_name
   - This command will create a new file


# Writing in a file

   - There are multiple ways to write in a file, and they are as follows:
       1. Using the redirection operator '>' and '>>'.
       2. Using an editor like vim or nano.
  
1. Using operators:
     - '>':
          - We can redirect the output of the command into a file using the '>' operator.
          - But '>' it overrides the existing content of the file.
      
     - '>>'
           - We can redirect the output of the command into a file using the '>>' operator.
           - '>>' append the output at the end of the existing content of the file.

       ![Diagram](https://github.com/Soham553/90DaysOfDevOps/blob/master/2026/day-06/Screenshot%202026-03-08%20124042.png)

2. Using Editor:
       - vim:
           - If a file is present, it will open the file in the editor
           - If a file is not present, it will create one and open it in the editor.
             
       - nano:
            - Same as vim

# Basic Command for reading and writing in a file:

    - cat cmd used to read the file in the current shell
    - head: used to print contaent of the files as per our need
         - -n: we can print several lines by passing the number instead of n
         - There are many other flags present as per need.
    - tail: output the last part of files
          - -n: It will count from the bottom of the file.
    - tee: read from standard input and write to standard output and files.
          - -a: append to the given files, do not overwrite.
   













    








