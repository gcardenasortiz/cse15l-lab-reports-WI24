# Report #5

## Original Post

<img width="567" alt="image" src="https://github.com/gcardenasortiz/cse15l-lab-reports-WI24/assets/156359594/87c3a62a-e6d7-4533-a67c-6a6658e797c6">


<img width="562" alt="image" src="https://github.com/gcardenasortiz/cse15l-lab-reports-WI24/assets/156359594/350ebe52-a87e-4bf3-b9a6-8f87864bc884">

Hi, when I run my `grade.sh` script locally on my computer it works perfectly fine but when I try to run it on the ieng6 server, it fails to compile. Could it have something to do with the fact that ieng6 is Linux? I'm running the script locally on a Macbook. 

## TA Response

Is the build that you're running locally up to date with the one on github? Try to use `git status` to make sure that this is the case. Is the `grading-area` directory on ieng6 the same as the one when you run it locally?

## Trying the command

<img width="581" alt="image" src="https://github.com/gcardenasortiz/cse15l-lab-reports-WI24/assets/156359594/89c72b65-6944-4531-ab76-981b9ca369f3">

<img width="624" alt="image" src="https://github.com/gcardenasortiz/cse15l-lab-reports-WI24/assets/156359594/9ef61a12-1bd6-4e59-a8cc-15b884058da5">

<img width="624" alt="image" src="https://github.com/gcardenasortiz/cse15l-lab-reports-WI24/assets/156359594/e245f136-80d5-4c34-8be0-e413aa0e29d1">

The build is up to date which means that they are the same builds, what seems to be wrong is that for some reason locally my script copies all the files while on ieng6 it copies the directory which messes up how the files are accessed by my script.

## Set-up

### File/Directory Structure

```
grader-review-gcardenasortiz/
|- GradeServer.java
|- TestListExamples.java
|- grade.sh
|- lib/
  |- hamcrest-core-1.3.jar
  |- junit-4.13.2.jar
|- Server.java
|- git-output.txt
|- grading-area/
|- student-submission/
  |- ListExamples.java
```

### Content of script before fix

<img width="552" alt="image" src="https://github.com/gcardenasortiz/cse15l-lab-reports-WI24/assets/156359594/2a5a4b1e-d586-47aa-b87e-465de883e519">

### Bug-Triggering Input

`bash grade.sh https://github.com/ucsd-cse15l-f22/list-methods-corrected`

### How to fix the bug

The bug seems to be a systems error, meaning it is entirely dependent on where the script is ran. To make it compatible with all systems you need to adjust 
