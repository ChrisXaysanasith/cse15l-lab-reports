# Lab Report 3

## Bugs and Commands

**Fail induced input**

`JUnit version 4.13.2
..E.E.E
Time: 0.004
There were 3 failures:
1) testReversed(ArrayTests)
array lengths differed, expected.length=2 actual.length=4; arrays first differed at element [2]; expected:<end of array> but was:<2>
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:89)
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:28)
        at org.junit.Assert.internalArrayEquals(Assert.java:534)
        at org.junit.Assert.assertArrayEquals(Assert.java:418)
        at org.junit.Assert.assertArrayEquals(Assert.java:429)
        at ArrayTests.testReversed(ArrayTests.java:18)
        ... 30 trimmed
Caused by: java.lang.AssertionError: expected:<end of array> but was:<2>
        at org.junit.Assert.fail(Assert.java:89)
        at org.junit.Assert.failNotEquals(Assert.java:835)
        at org.junit.Assert.assertEquals(Assert.java:120)
        at org.junit.Assert.assertEquals(Assert.java:146)
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:87)
        ... 36 more
2) reverseTestEven(ArrayTests)
arrays first differed at element [0]; expected:<1> but was:<6>
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:78)
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:28)
        at org.junit.Assert.internalArrayEquals(Assert.java:534)
        at org.junit.Assert.assertArrayEquals(Assert.java:418)
        at org.junit.Assert.assertArrayEquals(Assert.java:429)
        at ArrayTests.reverseTestEven(ArrayTests.java:25)
        ... 30 trimmed
Caused by: java.lang.AssertionError: expected:<1> but was:<6>
        at org.junit.Assert.fail(Assert.java:89)
        at org.junit.Assert.failNotEquals(Assert.java:835)
        at org.junit.Assert.assertEquals(Assert.java:120)
        at org.junit.Assert.assertEquals(Assert.java:146)
        at org.junit.internal.ExactComparisonCriteria.assertElementsEqual(ExactComparisonCriteria.java:8)
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:76)
        ... 36 more
3) reverseTestOdd(ArrayTests)
array lengths differed, expected.length=6 actual.length=3; arrays first differed at element [0]; expected:<1> but was:<3>
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:78)
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:28)
        at org.junit.Assert.internalArrayEquals(Assert.java:534)
        at org.junit.Assert.assertArrayEquals(Assert.java:418)
        at org.junit.Assert.assertArrayEquals(Assert.java:429)
        at ArrayTests.reverseTestOdd(ArrayTests.java:32)
        ... 30 trimmed
Caused by: java.lang.AssertionError: expected:<1> but was:<3>
        at org.junit.Assert.fail(Assert.java:89)
        at org.junit.Assert.failNotEquals(Assert.java:835)
        at org.junit.Assert.assertEquals(Assert.java:120)
        at org.junit.Assert.assertEquals(Assert.java:146)
        at org.junit.internal.ExactComparisonCriteria.assertElementsEqual(ExactComparisonCriteria.java:8)
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:76)
        ... 36 more

FAILURES!!!
Tests run: 4,  Failures: 3

`@Test
    public void reverseTestEven() {
    int[] input1 = {1, 2 ,3 ,4 ,5, 6};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{6, 5, 4, 3, 2, 1}, input1);
    }
`

`@Test 
    public void reverseTestOdd() {
    int[] input1 = {1, 2, 3};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{3, 2, 1}, input1);
    }
  `
  
**Doesn't induce failure**
`@Test 
    public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
    }
`

**Before and after code**
`static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
`

`static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length / 2; i += 1) {
      int temp = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = temp;
    }
  }
`

**grep -r**
look for all files in the current directory and in its subdirectories 
'shoot' technical/911report
![image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/fcf46c50-a503-4020-b9b5-3a7cc783132e)

**grep -c**
search and display the total number of times
* 'shoot' technical/911report/chapter-1.txt
![image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/c6fcbeb2-465e-4204-b5bd-d206259057ef)

**grep -iw** 
searching only the word
* "is" technical/911report/chapter-1.txt
![image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/ff3e9c8f-6e3d-4939-b7ea-71cdd79ae9eb)


**grep -n**
Display the matched lines and their line numbers
* "9/11" technical/911report/chapter-1.txt
![image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/b823f5cf-f4ef-4bfd-bdfb-2c6200b01284)

find ./technical/911report/ -iname "chapter-[0-12].txt"
finds the file name with the name in range
![image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/50dbca1b-6acd-49d9-869e-15b75de6fca3)

find ./technical/911report/ -name "*txt"
finds the file with txt extension
![image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/9bd5fc42-bd10-4455-a726-4a7ce393641d)

find ./technical/biomed/ -iname "1468-0678-3-[0.5].txt"
finds the file with txt extension
![image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/661d1a5d-6fbc-459d-ac8f-d09a89e9c911)

find ./technical/biomed/ -name "*txt"
finds the file with txt extension 
![image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/23ffeb95-b78c-4784-b049-039935e03c5e)


**Citation:**

ChatGPT - "what commands can i use with -name"

**ChatGPT output:**

"-name "file[0-9].txt": Use square brackets to match a single character from a specified range. This matches names like "file0.txt," "file1.txt," etc."
"-iname "pattern": This is similar to -name but performs a case-insensitive search. It matches "pattern" regardless of letter case."
"-name "*.txt": You can use wildcards to match files or directories with a specific extension. This example will find all files or directories ending with ".txt."

https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/

https://www.cyberciti.biz/faq/howto-use-grep-command-in-linux-unix/
