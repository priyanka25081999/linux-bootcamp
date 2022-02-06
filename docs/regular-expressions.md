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
