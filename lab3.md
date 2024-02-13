# **Lab Report 3:**
---
## **Part 1**
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


