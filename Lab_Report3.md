# Lab Report 3

## Part 1: Bugs

Failed:
``` @Test
public void testReverseInPlace2(){
  int[] input={1,2,3,4};
  ArrayExamples.reverseInPlace(input);
  assertArrayEquals(new int[]{4,3,2,1}, input);
}
```


The expected output for the array was {4,3,2,1} but instead, it was changed to the array {4,3,3,4}.

Didn't Fail:
``` @Test
public void testReverseInPlace() {
  int[] input1 = { 3 };
  ArrayExamples.reverseInPlace(input1);
  assertArrayEquals(new int[]{ 3 }, input1);
}
```


The symptom:![Image](Screenshot 2023-11-19 at 6.38.26 PM.png)
Code before:

```static void reverseInPlace(int[] arr) {
  for(int i = 0; i < arr.length; i += 1) {
  arr[i] = arr[arr.length - i - 1];
  }
}
```
Code after: 

```
static void reverseInPlace(int[] arr) {
  for(int i = 0; i < arr.length/2; i += 1) {
    int temp=arr[i];
    arr[i] = arr[arr.length - i - 1];
    arr[arr.length-i-1]=temp;
  }
}
```

The reason it wasn't working was that it wasn't being swapped but rather replaced. This is the reason it loses the value halfway through the array. The second reason was the for-loop traversed the entire list. Instead, you can grab the beginning of the array and then flip it to the other half.

##Part 2:

You can employ the find command in various ways to locate files or directories based on specific criteria. Here are some practical methods for using this command.


##find/list every directory

`$ find [directory] -type d`
This command will provide a list of all directories within a specified directory. It proves to be handy when you exclusively need to search for directories within a hierarchical directory structure. Here are a few examples to illustrate its usage.


```
$ find technical/government -type d
technical/government
technical/government/About_LSC
technical/government/Env_Prot_Agen
technical/government/Alcohol_Problems
technical/government/Gen_Account_Office
technical/government/Post_Rate_Comm
technical/government/Media
```



Above is the searching through and listing of each directory in `technical/government`.



```
$ find technical -type d
technical
technical/government
technical/government/About_LSC
technical/government/Env_Prot_Agen
technical/government/Alcohol_Problems
technical/government/Gen_Account_Office
technical/government/Post_Rate_Comm
technical/government/Media
technical/plos
technical/biomed
technical/911report
```



Above is useful for searching through and listing of each directory in `technical`. 


## Find/delete files
The command `$ find -name [name] -delete` is designed to locate and delete each file within a directory that matches the specified name. This command is a convenient way to eliminate all files that meet certain criteria within a directory with just a single command. Here are some examples to illustrate its usage.

```
$ find technical -name "chapter-1.txt" -delete
```


The command mentioned above doesn't generate any output; however, it effectively deletes the file named "chapter1.txt" within the "technical" directory.



```
$ find technical/government/Env_Prot_Agen "*.txt" -delete
```



The command presented above does not yield any output; nonetheless, it has deleted all files with names ending in ".txt" within the "technical/government/Env_Prot_Agen" directory.


## Find files greater

The `$ find [directory] -size [number][unit]` command is designed to locate and display all files within a directory based on their file size. This feature is highly valuable because it allows you to define a specific size and units (such as bytes, kilobytes, megabytes, etc.), and you can use "+" or "-" to list files larger or smaller than a designated size.



```
$ find technical/plos -size +29k
technical/plos/pmed.0020059.txt
technical/plos/pmed.0020073.txt
technical/plos/pmed.0020249.txt
technical/plos/pmed.0020103.txt
technical/plos/pmed.0010028.txt
technical/plos/pmed.0010064.txt
technical/plos/pmed.0020018.txt
technical/plos/pmed.0020182.txt
technical/plos/pmed.0020246.txt
technical/plos/pmed.0020045.txt
technical/plos/pmed.0010036.txt
```



The command displayed above scans the "technical/plos" directory and presents a list of files exceeding 29 kilobytes in size. The use of the "+" sign before 29 identifies files larger than the specified size (29), and the "k" denotes the unit of kilobytes.



```
$ find technical/911report -size -10000c
technical/911report
technical/911report/preface.txt
```


The command demonstrated above is conducting a search within the "technical/911report" directory and providing a list of files smaller than 10,000 bytes. It employs the "-" symbol before 10,000 to identify files with sizes less than the specified threshold (10,000), and the "c" designates the unit as bytes.


## Find files based on the time it was last modified

The command $ find technical -mtime [days] allows you to explore a designated directory and present a list of files and directories that have been modified within a specified time range. This functionality is advantageous as it enables you to search for both files and directories that were modified a precise number of days ago, within a defined range of days, or more than a certain number of days ago. You can achieve this by using the "+" or "-" symbols in your search criteria.


```
$ find technical -mtime -7
technical
technical/government
technical/.DS_Store
technical/plos/journal.pbio.0020010.txt
technical/911report
technical/911report/chapter-11.txt
```


The provided command is scanning the "technical" directory and compiling a list of files and directories that have undergone modifications in the previous 7 days. The use of the "-" sign before the number 7 specifies the search for files and directories modified within the specified number of days in the past.



```
$ find technical/plos -mtime +30
```




The command shown is searching through technical/plos to find files and directories that
have been modified greater than 30 days ago. The “+” in front of 30 is used to find files and
directories that have been modified greater than the specified number of days. No output was
produced, meaning that there are no files or directories in technical/plos that have been modified greater than 30 days ago.

*For each of the command shown, I used ChatGPT. Below is what I entered into ChatGPT, and the output that it produced*


![Image](6AB3BB96-9E25-4414-A07C-C26832A273FF.jpeg)

The command is useful for locating Specific Files, Recursive Search, and Combining with Other Commands.
