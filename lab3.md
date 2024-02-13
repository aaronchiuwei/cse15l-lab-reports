# Lab Report 3 - Bugs and Commands (Week 5)
# Part 1 - Bugs
**Failure Inducing Input**
```java
@Test
public void testFailure() {
  int[] input = {1, 2, 3};
  ArrayExamples.reverseInPlace(input);
  assertArrayEquals(new int[]{3, 2, 1}, input);
}
```
**No Failure Inducing Input**
```java
@Test
public void testNoFailure() {
  int[] input = {1};
  ArrayExamples.reverseInPlace(input);
  assertArrayEquals(new int[]{1}, input);
}
```
**Symptom**
<br> ![Image](Symptom.png)
<br>**Before Code Change**
```java
static void reverseInPlace(int[] arr) {
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = arr[arr.length - i - 1];
  }
}
```
**After Code Change**
```java
static void reverseInPlace(int[] arr) {
  int firstElem = arr[0];
  for(int i = 0; i < arr.length - 1; i += 1) {
    arr[i] = arr[arr.length - i - 1];
  }
  arr[arr.length - 1] = firstElem;
}
```
**Describe why the fix addresses the issue**
<br>The fix for reverseInPlace method changes the loop to 
not reach the last element and set the last element to the 
original first element. This addresses the issue of the last
element being set to the wrong element because the first 
element was already changed by storing the first element
and setting the last element to the stored element.
# Part 2 - Researching Commands
<br> 
