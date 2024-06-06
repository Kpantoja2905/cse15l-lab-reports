# ___Lab 4___ 

Overview 

During the lab, we implemented and practice coding within only the command line. This is especially usefule when we want to code within the `ieng6 server`. We learn how to edit and move around code within the terminal. 

> ## Log into ieng6 ##

First part of the lab was to long in to the `ieng6 server`. To log in to the `ieng6 server`, we can use the command ` ssh user@ieng6.ucsd.edu` which allows us to log in to the server through our terminal. Luckily we setup our `ieng6 server` so that we could easily log in to the server jsut using the command previously stated.

```
kevinpantoja@Kevins-MacBook-Air-5 ~ % ssh kpantoja@ieng6.ucsd.edu
Last login: Tue May 21 09:32:54 2024 from 100.90.245.169
Hello kpantoja, you are currently logged into ieng6-202.ucsd.edu

You are using 0% CPU on this system

Cluster Status 
Hostname     Time    #Users  Load  Averages  
ieng6-201   18:15:01   14  1.32,  0.71,  0.55
ieng6-202   18:15:01   13  0.16,  0.23,  0.19
ieng6-203   18:15:01   8   0.96,  0.56,  0.38

 

To begin work for one of your courses [ cs15lsp24 cs12sp24b ], type its name 
at the command prompt.  (For example, "cs15lsp24", without the quotes).

To see all available software packages, type "prep -l" at the command prompt,
or "prep -h" for more options.
[kpantoja@ieng6-202]:~:501$ cs15lsp24 
```

> ## Clone your fork of the repository from your Github account (using the SSH URL) ##

Once we were inside the server we had used the command `git clone` to clone the repositiory given to use in the Lab7, when the command was executed the command starts making a directory Lab7 with all the content of the repository. 

```
[kpantoja@ieng6-202]:kpantoja:507$ git clone https://github.com/ucsd-cse15l-s24/lab7.git
Cloning into 'lab7'...
remote: Enumerating objects: 62, done.
remote: Counting objects: 100% (2/2), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 62 (delta 0), reused 1 (delta 0), pack-reused 60
Receiving objects: 100% (62/62), 376.77 KiB | 1.23 MiB/s, done.
Resolving deltas: 100% (23/23), done.
[kpantoja@ieng6-202]:kpantoja:508$
```

> ## Run the tests, demonstrating that they fail

Once the repository was cloned into our server we can see the files within the repository using the command `ls` which is executed to list the content of the directory. As you can see below once we can see the contents of the directory, use run `bash test.sh ` that way we can run the test used on the java files.

```
[kpantoja@ieng6-202]:kpantoja:509$ cd lab7 
[kpantoja@ieng6-202]:lab7:510$ ls
ListExamples.java  ListExamplesTests.java  lib  test.sh
[kpantoja@ieng6-202]:lab7:511$ bash test.sh
JUnit version 4.13.2
..E
Time: 0.62
There was 1 failure:
1) testMerge2(ListExamplesTests)
org.junit.runners.model.TestTimedOutException: test timed out after 500 milliseconds
        at java.base/java.util.Arrays.copyOf(Arrays.java:3512)
        at java.base/java.util.Arrays.copyOf(Arrays.java:3481)
        at java.base/java.util.ArrayList.grow(ArrayList.java:237)
        at java.base/java.util.ArrayList.grow(ArrayList.java:244)
        at java.base/java.util.ArrayList.add(ArrayList.java:454)
        at java.base/java.util.ArrayList.add(ArrayList.java:467)
        at ListExamples.merge(ListExamples.java:42)
        at ListExamplesTests.testMerge2(ListExamplesTests.java:19)

FAILURES!!!
Tests run: 2,  Failures: 1

[kpantoja@ieng6-202]:lab7:512$ 
```

> ## Edit the code file to fix the failing test

As we can see the errors in the test come within the files of `ListExamples.java` being tested witht he tests within `ListExamplesTests.java` therfore we have to go into the `ListExamples.java` file in order to change the code that was being tested. Using the new command that we are able to learn in the lab called `vim`, we are able to edit the code within the terminal. We are able to learn about the command using the command called `vim tutor` which teaches us about the commands to use `vim`. We execute the command by entering `vim ListExamples.java` which opens the code in the terminal to look like.

We have the previous code which looked like:

![Image](https://github.com/Kpantoja2905/cse15l-lab-reports/blob/main/Screenshot%202024-05-22%20at%206.08.59%20PM.png?raw=true)

Using the typing `i` allows for use to insert changes within the code, which allows use to make the neccessary edits to the command. Which You can see we changed the code `index1 =` to `index2 =` in order for the code to run correctly. Although in vim it is a bit different to move around as I had to use the commands `<J> <L> <x> <A> <2> <esc> <:wq> ` in order ot get to the neccessary lines.

![Image](https://github.com/Kpantoja2905/cse15l-lab-reports/blob/main/Screenshot%202024-05-22%20at%206.09.39%20PM.png?raw=true)

> ## Run the tests, demonstrating that they now succeed
Once the changes were made to the java file, we could now run the `bash tests.sh` commands again in order to see if the new file passes the tests whcih you can see I executed the files below. Keys pressed: `<up> <up> <enter>`

```
[kpantoja@ieng6-202]:lab7:513$ bash test.sh
JUnit version 4.13.2
..
Time: 0.016

OK (2 tests)

[kpantoja@ieng6-202]:lab7:514$ 
```
> ## Commit and push the resulting change

For the final step 9, the keys were: `git<space>add<SPACE>.<ENTER>, git<space>commit<space>-m<space>"Changed were made"<ENTER>, git<space>push <ENTER>`
I used these git commands to commit and push the changes I made to the file onto the forked repo for this lab. I inculded a photo of my froked repo once I ran all my git commands

![Image](https://github.com/Kpantoja2905/cse15l-lab-reports/blob/main/Screenshot%202024-06-05%20at%2010.56.22%20PM.png?raw=true)


