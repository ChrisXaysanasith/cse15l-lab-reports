
**Student Symptom and Description of the Bug:**

Hello, this is my ListExamples where I want to identify the issues of why my run.sh file does not work when it tests the code? and why my script wont run the test file? There is also a bug in my merge code where it infintely runs. I assuming along the lines of it not having classes compiled, but it does show. For the merge, I am unsure on what I need to change in order to fix the loop, When I test with JUnit itself?

Can you help me identify the bug?


**Response from TA:** 

Can you please try running bash run.sh and showing me the bug?

**Student:**

<img width="962" alt="image" src="https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/8e2b39e2-ad07-45c3-9f03-61dc268fbebf">


**Reponse from TA:**

File structure:

<img width="301" alt="image" src="https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/2a70f071-9af3-4399-a848-0143656d648d">

**File of contents of the bug:**

<img width="802" alt="image" src="https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/b6d42d84-4b28-4eb8-b706-b0def4ba5fac">

<img width="719" alt="image" src="https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/9df351f1-45d7-4ea1-adc2-2ef13559993f">

<img width="687" alt="image" src="https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/b413a142-c869-4733-8713-12ef22c44518">


I recommend, you change the run.sh file to include `ListExamplesTest` rather than `ListExamplesTest.java` because it will result in error as you already compiled it.
In the merge code I suggest that you review your indexing and see which ones would match, for example index1 should stay as index1 += 1 and index2 should be index2 += 1. See if there is any noticable change that you should apply to fix the merge. But understanding your test file is actually well, it does work.

How I triggered the bug, was I ran `bash run.sh` which brought a JUnit Error.

<img width="979" alt="image" src="https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/eedaada4-9453-4815-96ae-3648ba7d4468">

The changes I made to `run.sh` was `ListExamplesTest.java` to `ListExamplesTest`

**Before:**

<img width="953" alt="image" src="https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/b8f395f8-ce92-46f8-a872-1e0b556db8d7">

**After:**

<img width="903" alt="image" src="https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/83e3d4f0-230a-4981-9a4d-5521e1630740">

Once, changed JUnit runs, as you said the merge code has an error to it

<img width="454" alt="image" src="https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/1b105f39-15f3-49ad-851b-51ab01c60382">

**Before:**

The error is within the code index1 += 1, the iteration is not set correctly rather it is index2 += 1

<img width="360" alt="image" src="https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/03348807-b4e2-406e-b63f-16cee46453c9">

**After:**

<img width="388" alt="image" src="https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/634bef40-c03a-4dfd-9160-b247c1fdc710">

Once all changes are applied it should be fixed

<img width="479" alt="image" src="https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/becd96b1-be54-41b5-9a63-b3b644469f79">

Part 2:

During my lab, I understood the commands but during outside time, I was behind in catching up the technical commands that we have learned in class. Reflecting the skill demo has been demonstrating a massive turn in how I could do something. Therefore, the knowledge that I have learned has put me into a factor of understanding terminal commands more and how I can use it wisely, precisionly in computer science. Such as Vim and Terminal, finding shortcuts in ways I can use it for the future.
