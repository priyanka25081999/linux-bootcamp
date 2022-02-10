**Some basic linux commands**

1. **find:**
2. **locate:**
3. **grep:**
4. **sed:**

**File and Text manipulation utilities:**
    
   The command line tools for manipulating text files:
    
    
   1. **cat:**
        
        It is short of *concatenate*, used to read and print files as well as viewing file contents. The main purpose of the cat command is to combine(concatenate)
        multiple files together.
     
       **Example:**
            
            * To view a file:
                  $ cat <filename>
       
   2. **tac:**
        
        It is used to print the lines of a file in a reverse order. Each line remains the same just order of lines is inverted.
        
        **Syntax:**
            
            $ tac <filename>
            $ tac file1 file2 > newfile
         
        **Example:**
        
            * To concate file and display output:
                    $ cat file1 file2
            * Combine and save output in a newfile:
                    $ cat file1 file2 > newfile
          
   3. **echo:**
        
        It displays(echos) the text. This *echo* command can be used to display a string on standard output (that is on terminal) or to place in a new file (using **>** operator) or append to an already exist file (using **>>** operator).
        The *echo* command is particularly useful for viewing the values of environment variables (built-in shell variables). For example, echo $USERNAME will print name of the user who has logged into the current terminal. 
        
        **Example:**
        
            * To put specified string in a newfile:
                    $ echo string > newfile
            * To display contents of environment variable:
                    $ echo $ENV_VARIABLE
            * To append a string into end of an already existing file:
                    $ echo string >> existing_file
            (We can deal with text, log, config, documentation files and many other file formats using this command)
       
   4. **head:**

        It reads the first few lines of each named file (by default - 10) and displays it on standard output. You can give a different number of lines in an option.
        
        **Example:**
            
            * To view first few lines of a file:
                    $ head sample_file.txt
            * To read first 5 lines of a file:
                    $ head -n 5 sample_file.txt
            
