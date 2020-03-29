> Sort function with mix file i.e. uppercase and lower case : When we have a mix file with both uppercase and lowercase letters then first the lower case letters would be sorted following with the upper case letters

```
Cat testfile.txt
March
August
February
January
September

$ sort testfile.txt
August
February
January
March
September
```
> Unix also provides us with special facilities like if you want to write the output to a new file, output.txt, redirects the output like this or you can also use the built-in sort option -o, which allows you to specify an output file.
Using the -o option is functionally the same as redirecting the output to a file.
```
$ sort -o output.txt testfile.txt
tuttu@tuttu-Inspiron:~$ cat output.txt 
abhishek
chitransh
divyam
harsh
naveen 
rajan
satish
```

> -r Option: Sorting In Reverse Order : You can perform a reverse-order sort using the -r flag. the -r flag is an option of the sort command which sorts the input file in reverse order i.e. descending order by default.
```
$ sort -r testfile.txt
satish
rajan
naveen 
harsh
divyam
chitransh
abhishek
```

> -n Option : To sort a file numerically used –n option. -n option is also predefined in unix as the above options are. This option is used to sort the file with numeric data present inside.
```
$ sort -n testfile.txt

1
3
5
44
78
95
908
```

> -k Option : Unix provides the feature of sorting a table on the basis of any column number by using -k option.
Use the -k option to sort on a certain column. For example, use “-k 2” to sort on the second column.

```
$ sort -k 2n testfile.txt
guard     3000
clerk    4000
peon     4500
manager  5000
employee  6000
director 9000
```

> -c option : This option is used to check if the file given is already sorted or not & checks if a file is already sorted pass the -c option to sort. This will write to standard output if there are lines that are out of order.The sort tool can be used to understand if this file is sorted and which lines are out of order
```
$ sort -c testfile.txt
sort: testfile.txt:2: disorder: clerk    4000
```

> -u option : To sort and remove duplicates pass the -u option to sort. This will write a sorted list to standard output and remove duplicates.
This option is helpful as the duplicates being removed gives us an redundant file.
```
$ sort -u testfile.txt > output.txt
tuttu@tuttu-Inspiron:~$ cat output.txt
clerk    4000
director 9000
employee 6000
guard    3000
manager  5000
peon     4500
```

> -M Option : To sort by month pass the -M option to sort. This will write a sorted list to standard output ordered by month name.

```
$ sort -M testfile.txt
January
February
March
August
September
```
