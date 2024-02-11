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

![Image](symp.png)

As you can see, there seems to be an issue with assigning the new values to their respective spots in the array in our method when we run the test that contains the above two inputs. 

**Bug Fix**

Before fixing it:
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i++) {
      arr[i] = arr[arr.length - i - 1];
    }
}
```
After fixing it:
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length / 2; i++) {
      int temp = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = temp;
    }
}
```

The issue was the logic behind overwriting the elements in the array. Before the array would use an already overwrittten element. However, by cutting the iterations in half and storing the value of the original index temporarily it allows us to succesfully overwrite each element without crossing over.

## Part 2
### The find command

**iname**



**type**
```
gcardenasortiz@Gwendals-Air technical % find ./ -type f
.//government/About_LSC/LegalServCorp_v_VelazquezSyllabus.txt
.//government/About_LSC/Progress_report.txt
.//government/About_LSC/Strategic_report.txt
.//government/About_LSC/Comments_on_semiannual.txt
.//government/About_LSC/Special_report_to_congress.txt
.//government/About_LSC/CONFIG_STANDARDS.txt
.//government/About_LSC/commission_report.txt
.//government/About_LSC/LegalServCorp_v_VelazquezDissent.txt
.//government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt
```
The `-type` option for the `find` command is useful for finding what we are looking for. In this case, we are trying to find only the files in a given directory.

```
gcardenasortiz@Gwendals-Air technical % find ./ -type d
./
.//government
.//government/About_LSC
.//government/Env_Prot_Agen
.//government/Alcohol_Problems
.//government/Gen_Account_Office
.//government/Post_Rate_Comm
.//government/Media
.//plos
.//biomed
.//911report
```
The `-type` option for the `find` command is useful for finding what we are looking for. In this case, we are trying to find only the directories in a given directory.

**links**



**print**
