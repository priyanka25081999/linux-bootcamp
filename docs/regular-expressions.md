**Regular Expressions and Search Patterns**

1. There are some text strings used for matching a specific patterns, or to search for a specific location, such as a start or end of a line or a word.
2. Regular expression can contain both normal characters as well as so called meta-characters such as * and $.


    
* **grep:**
      It is used as a primary text searching tool. It scans files for specified patterns and can be used with regular expression as well as simple strings.
      
     **Example:**

       |--------------------------------|-------------------------------------------------------------------------------------------------|
       |   Command                      |                                 Usage                                                           |
       |--------------------------------|-------------------------------------------------------------------------------------------------|
       | grep [pattern] <filename>      | Search for a pattern in a file and print all matching lines                                     |
       | grep -v [pattern] <filename>   | It prints all lines that do not match the pattern                                               |
       | grep [0-9] <filename>          | It prints the lines that contain the numbers 0 through 9                                        |
       | grep -C 3 [pattern] <filename> | It print context of lines for matching the pattern. Here, the number of lines is specified as 3 |
       |--------------------------------|-------------------------------------------------------------------------------------------------|
          
* **strings:** 
        It is used to extract all printable character strings found in the file or files given as an arguments. It is useful in locating human-readable content embeeded in binary files and for text files one can use grep command.
        
     **Example**
        
        * To search for the string my_string in a spreadsheet file:
              $ strings my_spreadsheet.xlsx | grep my_string
    
* **tr:**
        It is used to translate specified characters into other characters or delete them.
        
     **Syntax:**
            
      tr [options] set1 [set2]
            
     **Example:**

       |---------------------------------------------------|----------------------------------------------|
       |           Command                                 |                     Usage                    |                                                  
       |---------------------------------------------------|----------------------------------------------|
       | tr abcd ABCD                                      | Convert lower case to upper case             |
       | tr '{}' '()' <inputfile> outputfile               | Translate braces into parenthesis            |
       | echo "This is  a  test  file" | tr [:space:] '\t' | Translate white-space to tabs                |
       |---------------------------------------------------|----------------------------------------------|
          
* **tee:**
        'tee' takes the output from the command and while sending it to the stdout, it also saves it to a file. In simple words, it 'tees' the output stream from the command. One stream is displayed on the standard output and other is saved to a file. 
        
     **Example:**
        
        * To list contents of a directory on the screen and save the output of a file. The 'cat new-file' will show the output of 'ls -l' command.
            $ ls -l | tee new-file

* **wc:**
        wc (word count) counts the number of lines, words and characters in a file or list of files.
        
     **Example:**
     
        * Print only number of lines contained in a file:
            $ wc -l <filename>
       
     **options:**
        
        -l : displays the number of lines.
        -c : displays the number of bytes.
        -w : displays the number of words.

* **cut:**
        cut is used for manipulating column-based files and is designed to extract specific columns. The default column separator is the **tab** character. Basically the cut command slices a line and extracts the text. It is necessary to specify option with command otherwise it gives error. If more than one file name is provided then data from each file is not precedes by its file name.
        
     **Example:**
        
        * To display second column delimited by a blank-space(""):
            $ ls -l | cut -d "" -f 2  
            -d is used for delimiter and -f is the field number, in the above example field number is 2. To view the new output, do 'cut -f2 <filename>' in the command prompt.
        * To get specific column:
            $ cut -d " " -f 3 <filename>
            Here in this example, the field-number is 3.
          
