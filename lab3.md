# Lab Report 3

## Bugs and Commands

**Failure induced inputs**

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
 
![image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/843b8492-593d-4f15-8728-17b170fd9f5e)

**Doesn't induce failure**

`@Test 
    public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
    }
`

`@Test
  public void testReversed() {
    int[] input1 = {1, 2, 3, 4};
    assertArrayEquals(new int[]{4, 3, 2, 1}, ArrayExamples.reversed(input1));
  }
`

**Symptom**

![image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/dea61dd6-1cb6-4854-b32f-4f444362637d)

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

The first code does not work because the array does not have a temporary value to store the original to swap.

Therefore when we use the temp variable to store the original it allows the array to be reverse, We only need to check half of the array, to swap the other array. Which allows the elements to reverse.
The changes in this code allows a temp array to split allowing it to check half of the array to swap.

**grep -r**
look for all files in the current directory and in its subdirectories 
* `"shoot"` technical/911report
![image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/fcf46c50-a503-4020-b9b5-3a7cc783132e)

* `"stable"` technical/biomed
![image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/fcf46c50-a503-4020-b9b5-3a7cc783132e)

**This is important because it allows you to search for keywords recursively in the directory and its subdirectories if you are looking for a txt file that has it**

**grep -c**
search and display the total number of times
* `"shoot"`  technical/911report/chapter-1.txt
![image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/c6fcbeb2-465e-4204-b5bd-d206259057ef)

* `"stable"` technical/biomed/1468-6708-3-3.txt
![image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/54f2c502-e505-4478-8133-c0cb206241a7)

**This is important because it displays the amount of keywords in a txt file depending on what you are looking for**

**grep -iw** 
searching only the word
* `"is"` technical/911report/chapter-1.txt
![image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/ff3e9c8f-6e3d-4939-b7ea-71cdd79ae9eb)

* `"3"` technical/biomed/1468-6708-3-3.txt
![image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/a44221ff-3e5b-413d-8692-7254ee998e44)

**This is searching for the word in a txt file therefore it shows the concurrent amount of time it appears**

**grep -n**
Display the matched lines and their line numbers
* `"9/11"` technical/911report/chapter-1.txt
![image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/b823f5cf-f4ef-4bfd-bdfb-2c6200b01284)

* `"disease"` technical/biodmed/1408-3-1.txt
![image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/52c9170d-f0ab-4fb9-8c32-a9e18d194e78)

**This shows the matched line depending on what you are looking for in a txt file and it shows the content of the line it is at**

**Citation:**

These are the sources I used for -r, -c, iw, -n 

![image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/e12ab5d9-1e25-48a0-aa1d-38515f78c0a4)

![image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/2842fae6-dfc6-4666-b96e-9c37cd20c268)

![image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/aa56e77e-bee0-4780-8068-5dd61fe5ace8)

![image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/da85b86f-4cb3-4887-abae-1f7483ed7ef6)

https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/

https://www.cyberciti.biz/faq/howto-use-grep-command-in-linux-unix/
