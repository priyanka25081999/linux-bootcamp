In managing files, one may need to perform serveral tasks such as sorting data, copying data from one source location to another, split the file data and many others.

You can use below utilities to manage files:
	1. sort
	2. uniq
	3. paste
	4. join
	5. split

1. Sort:
	It is used to rearrange the lines of a test file either ascending or descending order, according to sort key. The default sort key is the order of ASCII characters (essentially alphabetically).

        Syntax:
	   sort <filename>
	
	Example:
           |---------------------------------------------------|
	   |      Command	   |      Description          |
	   |---------------------------------------------------|
	   |cat file1 file2 | sort | Combine 2 files, sort     |
	   |			   | the lines and display the |
	   |	         	   | output on the terminal    |
           |---------------------------------------------------|
           |sort -r <filename>     | Sort the lines in reverse |
           |                       | order                     |
           |---------------------------------------------------|
       
	* -u option : Sort checks for unique values after sorting the records(lines). It is equivalent to running uniq on the output of sort.
        * -k option : Sort the lines by the nth field on each line instead of the beginning.


