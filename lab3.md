# **Lab Report 3:**
---
## **Part 1 - Bugs**
The method from the `ArrayExamples.java` that the test cases are being tested on are:
```java
public class ArrayExamples {

  // Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
From the `ArrayTests.java`
* A failure-inducing input for this buggy program, as a JUnit test and any associated code:
```java
public class ArrayTests {
	@Test 
	public void testReverseInPlace2() {
    int[] input1 = {1, 2};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{2, 1}, input1);
	}
```
* An input that doesn't induce a failure, as a JUnit test and any associated code:
```java
public class ArrayTests {
	@Test 
	public void testReverseInPlace() {
    int[] input1 = {2};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{2}, input1);
	}
```
* The symptom, as the output of running the tests:
* The array {1, 2} are not being reversed correctly as {2, 1}
!Image
* The bug, as the before-and-after code change required to fix it:
  - Before the code change:
  ```java
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
  ```
  - After the code change:
  ```java
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      int temp = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = temp;
    }
  }
  ```
* Why the fix addresses the issue?
  - By introducing a variable `temp`, it stores the value of `arr[i]` inside before it gets overwritten. And as for the original code, since the original values in the array are not being saved, when going over the iteration, all the element are being overwritten and becomes the same. But by saving and stores the element's original value into `temp`, the swap of the values happens correctly with the rescue of the original values of the array.
---
## **Part 2 - Researching Commands**
Information about the command `grep`
**Option 1:**
* -c, --count: counts the matching lines for each input file or directories 
  1) ```java
     grep -c "it" ./technical/biomed/cc300.txt
     119
  	 ```
  2)


