Create a file named notes.txt
Write 3 lines into the file using redirection (> and >>)
Use cat to read the full file
Use the head and tail to read parts of the file
Use a tee once to write and display at the same time
Keep it short (8–12 lines total in the file)
Suggested command flow:

touch notes.txt
echo "Line 1" > notes.txt
echo "Line 2" >> notes.txt
echo "Line 3" | tee -a notes.txt
cat notes.txt
head -n 2 notes.txt
tail -n 2 notes.txt


# Creating a new File
   - touch file_name
   - This cmd will create a new file


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

2. Using Editor:
       - vim:
           - If a file is present, it will open the file in the editor
           - If a file is not present, it will create one and open it in the editor.
             
       - nano:
            - Same as vim







