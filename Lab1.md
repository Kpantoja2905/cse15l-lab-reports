# ___Lab 1 Report___

> ## Overview

During the lab we were able to put in practice of the knowledge of commands were were able to learn about from lectures. We used the VScode terminal to be able to implement the practice of our commands which we were able to set up as shown below.

![Image](https://github.com/Kpantoja2905/cse15l-lab-reports/blob/main/Screenshot%202024-04-02%20at%209.38.01%20AM.png?raw=true)

During this week 1 Lectures we learned commands such as `cd`, `ls`, and `cat`. The commands are used in order to be able to access and see specific files or directories. During the lab, we put the following commands into practice by using the commands to change or access specific directories from the repository that we were able to clone for GitHub using the command `git clone` which allowed us to clone into our VS code terminal in order to execute the commands we learned in lecture.

![Image](https://github.com/Kpantoja2905/cse15l-lab-reports/blob/main/Screenshot%202024-04-02%20at%209.49.12%20AM.png)

> ## Changing Directory

In the following Example, I am starting off in the `/home` directory, denoted by the`~`.

```
kevinpantoja@Kevins-MacBook-Air-5 ~ % 
```

During that lab one of the commands we were implementing into our lab was the use of `cd` which will change the directory of the current working directory based on the arguements provided to the code. Without the use of an arguement the `cd` command will return me to the `/home` directory. Given an arguement the the `cd` command will change the current working directory. This can be proven using the command `pwd` which prints the current working directory. This can be seen in the following Example:

```
kevinpantoja@Kevins-MacBook-Air-5 ~ % cd Desktop
kevinpantoja@Kevins-MacBook-Air-5 Desktop % pwd
/Users/kevinpantoja/Desktop
kevinpantoja@Kevins-MacBook-Air-5 Desktop % 
```

The way were were able to implement the cd command in our lab in order to change our directory from the home directory to the lecture1 directory.

![Image](https://github.com/Kpantoja2905/cse15l-lab-reports/blob/main/Screenshot%202024-04-10%20at%204.44.33%20PM.png?raw=true)

1) As seen in the image above, when executed without an arguement the `cd` command will take us to our `/home` directory also denoted as `~`. Before the command executed it was

```
   /Users/kevinpantoja
This it became:
   /Users/kevinpantoja
```

2) When the command was executed with the arguement `lecture1`, the command change the directory to `lecture1`.

```
   /Users/kevinpantoja
This it became:
   /Users/kevinpantoja/lecture1
```

3) When the `cd` command was executed with the file `Hello.java`, the command had an error because the arguement was not a directory.


> ## List Directory

The lab allowed us the practice the implementation of the `ls` command which allows us to list out the the files and directories within the current working directory if not given an arguement. When given an arguement, the `ls` command will list out the the files and directories within the the directory given in the arguement.  

![image](https://github.com/Kpantoja2905/cse15l-lab-reports/blob/main/Screenshot%202024-04-10%20at%204.45.05%20PM.png?raw=true)

1) As shown in the image, when the `ls` command is executed with no arguement given the, command will print all the files and directories in the current working directory such as in the image all the files and directories in my Desktop are printed after the `ls` command was executed.
```
kevinpantoja@Kevins-MacBook-Air-5 lecture1 % pwd
/Users/kevinpantoja/lecture1
kevinpantoja@Kevins-MacBook-Air-5 lecture1 % ls
Hello.class     Hello.java README               messages
```
2) When the `ls` command is executed with a directory, the command will print the content of the directory in the arguement.
```
kevinpantoja@Kevins-MacBook-Air-5 lecture1 % pwd
/Users/kevinpantoja/lecture1
kevinpantoja@Kevins-MacBook-Air-5 lecture1 % ls messages/
en-us.txt       es-mx.txt  zh-cn.txt
```
3) When the command is executed with a file such as `Hello.java` the output will be the name of that file.
```
kevinpantoja@Kevins-MacBook-Air-5 lecture1 % pwd  
/Users/kevinpantoja/lecture1
kevinpantoja@Kevins-MacBook-Air-5 lecture1 % ls Hello.java
Hello.java
```

> ## Catenation

The `cat` command allowed us to view the contents of a file in the lab. When the command is used, the command must be used with an argument. The command runs an error when the command is used with a directory such as `messages` shown below. But when the command is executed with a file such as `Hello.java` the command prints out the contents within the file.

![image](https://github.com/Kpantoja2905/cse15l-lab-reports/blob/main/Screenshot%202024-04-10%20at%204.46.54%20PM.png?raw=true)
