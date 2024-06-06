# Lab Report 5

## Piazza Post

> ## **Question @1**
> 
> 101 views
>
> **Debugging Error**
>
> Hi everyone,
>
> I'm having an issue with the filter method in our assignment. The method is supposed to filter a list of strings based on a StringChecker implementation and return a new list with the elements that pass the check, in the same order they appeared in the input list. However, the order of elements in the resulting list is reversed. Here is my code: 
>
> ![Image](https://github.com/Kpantoja2905/cse15l-lab-reports/blob/main/Screenshot%202024-06-05%20at%2011.21.59%20PM.png?raw=true)
>
> 
> ## TA Response
> 
>Good observation! The issue is with the line `result.add(0, s);` in the `filter` method. Adding elements at index `0` inserts them at the beginning of the list, causing the order to be reversed. To maintain the original order, you should add elements to the end of the list.
>
> ## Student Screenshot
>
> Thank you for the quick response! I updated the filter method as you suggested. I was able to switch the part where within the ListExamples.java the code inserts the element to the back of the list rather than inserting the code in the beginning. I was able to change the code using the `vim` command on the `ListExamples.java` since when I had ran `bash test.sh` that was file that had the recurring message of an error. 
> 
> ![Image](https://github.com/Kpantoja2905/cse15l-lab-reports/blob/main/Screenshot%202024-06-05%20at%2011.24.35%20PM.png?raw=true)



## Reflection 

Learning Vim during the best part of the quarter means you had a good opportunity to focus on it without too many other distractions. Here's why it's beneficial for programming on the command line. Vim is a highly efficient text editor that allows you to edit files quickly using keyboard shortcuts. This saves time compared to using a mouse. Vim works in the command line, so you can edit code directly on remote servers or within your terminal without needing a graphical interface. Learning Vim helps you become more comfortable with command-line tools and environments, which are essential for many programming and system administration tasks. So, dedicating a good part of your quarter to learning Vim means you gained a valuable skill that makes you a more efficient and capable programmer, especially when working directly in the command line.

