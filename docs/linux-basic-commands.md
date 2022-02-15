* **Some basic linux commands**

1. **find:**
2. **locate:**
           
      Another method of locating files is provided by the *locate* command. It searches entire filesystem(except for paths which have been excluded) and works off a database that is updated. That's why it is very fast. 
      It looks into it's database and reports the file location. *find* command doesn't use any database. It traverses all the directories and looks for files matching the given criterion. 
      *locate* will only able to find files that were already in existence the last time the database was updated. For more details of the command type *locate --help* on terminal.
      
      **Example:**
            
            * To find all files on your system that have '.conf' in them:
                 $ locate .conf

3. **grep:**
            
      It is a utility whose job is to search files for patterns and print out matches according to specified options. It basically stands for global regular expression print and it can work with more complicated regular expression which can contain wildcards and other special attributes.
      
      **Syntax:**
      
            |--------------------------------------------------------------------------------|
            |      Command	                        |      Description                    |
            |--------------------------------------------------------------------------------|
            | grep [pattern] <filename>                | Search for a pattern in a file      |
            |		                                | and print all matching lines        |
            |--------------------------------------------------------------------------------|
            | grep -v [pattern] <filename>             | Print all lines that do not         |
            |		                                | match the pattern                   |
            |--------------------------------------------------------------------------------|
            | grep [0-9] <filename>                    | Print the lines that contain        |
            |                                          | the numbers 0 through 9             |
            |--------------------------------------------------------------------------------|
            | grep -C 3 [pattern] <filename>           | Print context of lines (specified   |
            |                                          | number of lines above and below the |
            |                                          | pattern) for matching the pattern;  |
            |                                          | here, the number of lines is        |
            |                                          | specified as 3                      |                 
            |--------------------------------------------------------------------------------|
      
      
     **Examples:** 

            1. To find the pattern "dog" in the file:
                      $ grep dog sample_file.txt
                      
            2. To search the pattern "dog" and "cat" in all files of current directory by ignoring case:
                      $ grep -i -e dog -e cat -r .
                
                   -i -> ignore case
                   -e -> use the next given pattern/string/special character for search
                   -r -> recurse through sub-directories
                   
            3. To print all lines start with word "dog":
                      $ grep "^dog" sample_file.txt
                      
            4. To print all lines end with word "dog":
                      $ grep "dog$" sample_file.txt
                      $ grep d[a-p] sample_file.txt     
      
4. **sed:**

      In order to create and then edit or extract contents from a file repetatively, this command can be used. sed stands for stream editor. Using this command, we can perform lots of functions on file like searching, find and replace, insertion or deletion. Also we can edit a file without opening it. 
        
      **Example:**
      
            |--------------------------------------------------------------------------------|
            |      Command	                        |      Description                    |
            |--------------------------------------------------------------------------------|
            | sed s/pattern/replace_string/ file       | Substitute first string occurrence  |
            |		                                | in every line 		      |
            |--------------------------------------------------------------------------------|
            | sed s/pattern/replace_string/g file      | Substitute all string occurrences   |
            |		                                | in every line                       |
            |--------------------------------------------------------------------------------|
            | sed 1,3 s/pattern/replace_string/g file  | Substitute all string occurrences   |
            |                                          | in a range of lines                 |
            |--------------------------------------------------------------------------------|
            | sed -i s/pattern/replace_string/g file   | Save changes for string substitution|
            |                                          | in the same file                    |
            |--------------------------------------------------------------------------------|

* **File and Text manipulation utilities:**
    
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
   5. **tail:**
            
        It reads the last few lines of each named file (by default - 10) and displays it on standard output. You can give a different number of lines in an option. *tail* is mostly useful when you are troubleshooting any issue using log files, as you want to see the most recent lines of output.
        
        **Example:**
        
            * To view last few lines of a file:
                    $ tail sample_file.txt
            * To read last 15 lines of a file:
                    $ tail -n 15 sample_file.txt
            * To continously read output of growing log file:
                    $ tail -f sample_file.log
            
            The third command will continously display new lines of output in sample_file.log as soon as they appear. Thus, it enables user to monitor any current activity that is being reported and recorded.


* **Viewing compressed files:**
        
        
    To work with compressed files, the associated utilites have the letter 'z' prefixed to their name. For example, zcat, zless, zdiff and zgrep. These commands are used to search the contents of a compressed file without uncompressing it. It can be used with other options to extract data from the file, such as wildcards.
        
     **Example:**
        
        * To view contents of compressed file:
              $ zcat compressedfile.txt.gz
                   
