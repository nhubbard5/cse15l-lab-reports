# __Lab Report 3__  
November 5, 2023  
Nicholas Hubbard  

## Part 1
The Buggy Program:  
~~~
static int[] originalReversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
~~~  


Failure-Inducing Input for the Buggy Program:  
~~~
@Test
  public void testOriginalReversed() {
    int[] input1 = {1, 2, 3};
    assertArrayEquals(new int[] {3, 2, 1}, ArrayExamples.originalReversed(input1));
  }
~~~  

Non-Failure-Inducing Input for the Buggy Program:  
~~~
@Test
  public void testOriginalReversedNoFailure() {
    int[] input1 = {};
    assertArrayEquals(new int[] {}, ArrayExamples.originalReversed(input1));
  }
~~~

The Symptom:  
![Code](report3screenshot1.png)  

The buggy code was shared at the start of this report.    
The new code:
~~~
static int[] fixedReversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }
~~~

The old code was incorrect because it was trying to put the values of the holder\`newArray array into the input \`arr array, and then return the input array. The new code solves this problem by moving the input array's values into the newArray from back-to-front, then returning the newArray.  

## Part 2  
Let's look at the `find command.  
Here are 4 interesting command-line options:  
1. -type

The first example I will show is -type d, where d means directory.  
~~~
find technical/ -type d
technica/
technical/911report
technical/biomed
technical/government
technical/government/About_LSC
technical/government/Alcohol_Problems
technical/government/Env_Prot_Agen
techncial/government/Gen_Account_Office
technical/government/Media
technica/government/Post_Rate_Comm
technical/plos
~~~
The second example is with -type f, for normal files.
~~~
$ find technical/ -type f > type-f-results.txt
wc type-f-results.txt
1391 1391 54178 type-f-results.txt
~~~

Using -type followed by a letter corresponding to a type of result will limit results to just the requested type. This command is useful when searching huge directories of different file types.

2. -maxdepth
4. -name
5. -delete
