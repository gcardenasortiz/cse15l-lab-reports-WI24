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

The second input seems to fail due to a flawed implementation of the reverseInPlace method.

**Successful Input**
```
@Test 
public void testReverseInPlace() {
  int[] input1 = {3};
  ArrayExamples.reverseInPlace(input1);
  assertArrayEquals(new int[]{3}, input1);

  ...
}
```

However, the first input of this test seems to work just fine.

**Symptom**
![Image](sym.png)

As you can see, there seems to be an issue with assigning the new values to their respective spots in the array in our method when we run the test that contains the above two inputs. 
**Bug Fix**

## Part 2
