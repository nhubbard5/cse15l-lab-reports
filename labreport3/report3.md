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

