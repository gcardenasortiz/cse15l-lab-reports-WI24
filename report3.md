# Report #3
## Part 1
**Failure Inducing Input**
```
@Test 
public void testReverseInPlace() {
  ...

  int[] input2 = {3, 2, 1};
  ArrayExamples.reverseInPlace(input2);
  assertArrayEquals(new int[]{1, 2, 3}, input2);
}
```

The second input seems to fail due to a flawed implementation of the reverseInPlace method. Which shows us this error in the terminal:
```
arrays first differed at element [2]; expected:[3] but was:[1]
 at ArrayTests.testReverseInPlace(ArrayTests.java:13)
Caused by: java.lang.AssertionError: expected:[3] but was:[1]
 ... 31 more
```

**Successful Input**
```
@Test 
public void testReverseInPlace() {
  int[] input1 = {3};
  ArrayExamples.reverseInPlace(input1);
  assertArrayEquals(new int[]{3}, input1);

  ...
```

However, the first input of this test seems to work just fine.

**Symptom**

static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i++) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```

**Bug Fix**

## Part 2
