# Lab Report 2: Servers and Bugs

## Part 1:

## Part 2:

For this part of the lab report, I am going to explain the bugs in the reversed method in the file ArrayExamples.java
- A failure inducing input for this method was the following JUnit test:

`
@Test

public void testReversed1() {

  int[] input1 = { 6, 7 };
  
  assertArrayEquals(new int[]{ 7, 6 }, ArrayExamples.reversed(input1));
  
}
`
 
 
- A input that did not induce a failure for this method is the following JUnit test:

`
@Test

public void testReversed() {

  int[] input1 = { };
  
  assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  
}
`


- The system of the bug in this method, that is the output when I ran these two tests in JUnit:


- The bug in the code:

1. The code before the change (with the bug) :

  `
  static int[] reversed(int[] arr) {
  
    int[] newArray = new int[arr.length];
    
    for(int i = 0; i < arr.length; i += 1) {
    
      arr[i] = newArray[arr.length - i - 1];
      
    }
    
    return newArray;
    
  }
  `
  
  
2. The code after the change (the bug was removed/fixed):

  `
  static int[] reversed(int[] arr) {
  
    int[] newArray = new int[arr.length];
    
    for(int i = 0; i < arr.length; i += 1) {
    
      newArray[i] = arr[arr.length - i - 1];
      
    }
    
    return newArray;
    
  }
  `
  
