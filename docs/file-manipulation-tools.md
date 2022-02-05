In managing files, one may need to perform serveral tasks such as sorting data, copying data from one source location to another, split the file data and many others.

You can use below utilities to manage files:

	1. sort
	2. uniq
	3. paste
	4. join
	5. split
	6. wc

1. **sort**:
	
	It is used to rearrange the lines of a test file either ascending or descending order, according to sort key. The default sort key is the order of ASCII characters (essentially alphabetically).

	**Example**:
	
       |---------------------------------------------------|
	   |      Command	        |      Description          |
	   |---------------------------------------------------|
	   | sort <filename>       | sorts the file according  |
	   |		        | to sort key		    |
	   |---------------------------------------------------|
	   | cat file1 file2 | sort| Combine 2 files, sort     |
	   |		        | the lines and display the |
	   |	                | output on the terminal    |
       |---------------------------------------------------|
       | sort -r <filename>    | Sort the lines in reverse |
       |                       | order                     |
       |---------------------------------------------------|
       
	* -u option : Sort checks for unique values after sorting the records(lines). It is equivalent to running uniq on the output of sort.
     * -k option : Sort the lines by the nth field on each line instead of the beginning.

2. **uniq**: 

	uniq removes the duplicate consecutive lines in a text file. It is useful for simplefying text display.
	
	**Example**:

		* To remove duplicate entries from multiple files at once:
			$ sort file1 file2 | uniq > file3
			$ sort -u file1 file2 > file3
		* To count the number of duplicate entries:
			$ uniq -c <filename>
			
	Because uniq requires that duplicate entries must be consecutive, one often runs **sort** first and then pipes the output into **uniq**. If sort is used with the **-u** option, it can be do it in one step.

3. **join**:
	
	This command is used to combine two files on a common field. It is also used to join the two files based on a key field present in both the files. The input file can be separated by white space or any delimiter.
	
	**Example**:
	
		$ join file1 file2

4. **split**:

	To split a file in different parts that is breaks up a file in different line segments this command is used. It is used to split large files into smaller files. It splits the files into 1000 lines per file(by default) and even allows users to change the number of lines as per requirement.
	
	**Example**
		
		* To split a file in small parts:
			$ split <filename> 
		* To split a file based on line numbers:
			$ split -l number <filename1> <filename2>
		* To split a file in specific numbers:
			$ split --number=number <filename>

5. **paste**:
	
	It can be used to combine fields (such as phone number) from different files, as well as combine files from multiple files. For example, line1 from file2, line2 from file1 can be combined with line2 of file2 and so on.
	
	**Example**:
	
		* To paste contents from 2 files:
			$ paste file1 file2
		* Use of delimiter(here comma is used as delimiter):
			$ paste -d , file1 file2

6. **wc**:
	
	It is used to count the words of a file. wc stands for **word count**. It is used to find out number of lines, word count, byte and characters count in the files specified in the file arguments. By default it displays four-columnar output. First column shows number of lines present in a file specified, second column shows number of words present in the file, third column shows number of characters present in file and fourth column itself is the file name which are given as argument.
	
	**Example**:
		
		$ wc <filename>
		$ wc -l <filename> 
	* -l option is used to print number of lines present in a given file. 
	* -w option is used to print number of words present in a given file. 
	* -c option is used to count number of bytes present in a given file. 
	* -m option is used to display count of charaters from a given file. 
	* -L option is used to print length of longest line in a given file.
