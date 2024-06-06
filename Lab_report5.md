# Lab Report 5

## Piazza Post

> ## **Question @1**
> 
> 101 views
>
> **Debugging Error**
>
> There was an issue while running the program for Lab 7. I ran the test in order to test the java files within the Lab 7 directory, but when I ran the test using the `bash test.sh` command, the test failed. I had made sure that the java files compiles correctly by using the command `javac *.java` but the test are still failing.
>
> ![Image](https://github.com/Kpantoja2905/cse15l-lab-reports/blob/main/Screenshot%202024-06-05%20at%205.10.36%20PM.png?raw=true)
>
> ## TA Response
> 
>Assuming that the files have complied correctly, the bug while running your command has to be coming within the actual code within the java files. You could access the files in order to debug the class using the `vim` command.
>
> ## Student Screenshot
>
> I was able to access the class using the `vim` command but I was not able to tell where the error is within the java file. I know that the java files are failing the test.
> 
> ![Image](https://github.com/Kpantoja2905/cse15l-lab-reports/blob/main/Screenshot%202024-06-05%20at%205.53.01%20PM.png?raw=true)
>
>  ## TA Response
>
> When you ran the test for the java files using the `bash test.sh`, the test results tell you an idea of where the bug is. Below you can see your test results is failing:
>
> ```
> JUnit version 4.13.2
> ..E
> Time: 0.523
> There was 1 failure:
> 1) testMerge2(ListExamplesTests)
> org.junit.runners.model.TestTimedOutException: test timed out after 500 milliseconds
>         at ListExamples.merge(ListExamples.java:44)
>         at ListExamplesTests.testMerge2(ListExamplesTests.java:19)
>
> FAILURES!!!
> Tests run: 2,  Failures: 1
> ```
>
> As you can see your test is failing around line 44 within the ListExamples.java
>
> ## Student Screenshot
>
> I was able change the index from index1 to index 2 in order for merge method to work
> 
> ![Image](https://github.com/Kpantoja2905/cse15l-lab-reports/blob/main/Screenshot%202024-06-05%20at%205.51.47%20PM.png?raw=true)

## 
