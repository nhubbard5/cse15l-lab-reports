# __Lab Report 3__  
November 5, 2023  
Nicholas Hubbard  

##Part 1
~~~@Test
  public void testOriginalReversed() {
    int[] input1 = {1, 2, 3};
    assertArrayEquals(new int[] {3, 2, 1}, ArrayExamples.originalReversed(input1));
  }
