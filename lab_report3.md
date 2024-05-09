# ***Lab Report 3***

## **Bugs (Part 1)**

I have choosen to explore the `LinkedListExample.java` file from the `class LinkedList` from the Week 4 Lab to explore the bug within the code in the `append()` method.


The following input should return a failed test because the append method is used to add elements in the `LinkedList` and in the following coed, it can be seen that the code is meant to add two elements within the `new LinkedList()` but the test expected value says the there is only one element. But during our lab that code was fixed in order for this test to pass.

  ```
  @Test
  public void testAppendBug(){
    LinkedList list= new LinkedList();
    list.append(1);
    list.append(2);

    assertEquals(1,list.length());
  }
  ```

Meanwhile the following test should be successful because the code determines that the `new LinkedList()` will add 3 elements which is the same as the expected output within the test. Similarily, before chenges are made this test fails but when the bugs are corrected, the test will pass.

  ```
  @Test
  public void testAppendBug(){
    LinkedList list= new LinkedList();
    list.append(1);
    list.append(2);

    assertEquals(1,list.length());
  }
  ```

Thefore as mentioned above when the code is fixed, the `test` outputs will change because the code will produces the correct out therefore the test that are meant to pass, will pass whereas the test that are meant to fail, will fail.

BEFORE:
  ```
  public void append(int value){
    ---PREVIOUS CODE---
    while (n.next !=null){
      n = n.next;
      n.next= New Node (value, null);
    }
  }
  ```

AFTER:
  ```
  public void append(int value){
    ---PREVIOUS CODE---
    while (n.next !=null){
      n = n.next;
    }
    n.next= New Node (value, null);
  }
  ```

The bug within the code was the fact that after the first iteration of the while loop, the code will no longer iterate because, within the while loop, the `n.next` is assigned a `new Node` where the value is `null`. So therefore when the code is ran again and `append` method is used a second time, it does not reassign the `null` value because it does not pass the conditional statement within the while loop since `n.next` is `null`.

## **Researching Commands (Part 2)**

The `grep` command is the command that intereset in me in the Lab therefore I wanted to be able to explore the command.

> Example Command 1 :

`grep` has the command `-i`, which ignores case distinctions when matching patters, in the following example, I input the `grep -i "doctor" *.txt` to search through all the txt files in the biomed folder for the word "doctor" regardless of its case. It then returns all the files that contain the given word.

```
kevinpantoja@Kevins-MacBook-Air-5 biomed % grep -i "doctor" *.txt
1471-2156-4-10.txt:  Cynthia Coffman is the post-doctoral...
1471-230X-1-6.txt:   effects (Figure 1) is striking..
---SEVERAL OTHER LINES---
```

>  Another Example:

The command was no longer in the terminal but can be seen a the bottom of my example. The code was implemented to find the lines that include the given pattern while ignoring the case distinctions.

```
pro_bono_efforts.txt:"If they do it, that's what all lawyers should be doing."
pro_bono_efforts.txt:For more than a decade, lawyers at corporations such as Cinergy
pro_bono_efforts.txt:lawyers.
pro_bono_efforts.txt:But large law firms just now are getting organized to do similar
pro_bono_efforts.txt:Smaller firms also stepped up their efforts. All 35 lawyers at
pro_bono_efforts.txt:The firm will not set a companywide goal for all lawyers to meet
pro_bono_efforts.txt:lawyers for pro bono work is out of the question.
pro_bono_efforts.txt:"We could throw as many lawyers as we can get at the poor and
residents_sue_city.txt:On Friday, a group of residents filed a lawsuit against
residents_sue_city.txt:The lawsuit, filed by attorneys for Neighborhood Legal Services
residents_sue_city.txt:lawsuit. He said the city still maintains that the residents of the
water_fees.txt:Legal Services, is building a lawsuit against Alpaugh

kevinpantoja@Kevins-MacBook-Air-5 media % grep -i "law" *.txt
```

> Example Command 2 :

`grep` has the command `-v`, which prints out the lines that do not match the pattern, in the following example where the command goes through the lines that did not contain the given pattern.

```
kevinpantoja@Kevins-MacBook-Air-5 media % grep -v "police" *.txt
5_Legal_Group.txt
...
5_Legal_Group.txt: BY EDWARD MCDONOUGH
---SEVERAL OTHER LINES---
```

>  Another Example:

The following Example prints out the lines that do not match the pattern `"law"` and then prints out the lines.


```
kevinpantoja@Kevins-MacBook-Air-5 media % grep -v "law" AP_LawSchoolDebts.txt

The Associated Press

Law school debts forcing recruits to private sector
November 18, 2002
government or public advocacy groups because their need for money
to pay off massive student loans leads them to the more lucrative
private sector, a study being released Monday found.
Legal education debt, which tops $84,000 for the average new
interest jobs, according to the joint study by Equal Justice Works,
the National Association for Law Placement and the Partnership for...
```

> Example Command 3 :

`grep` has the command `-E`, which is used to change the patterns as extended regular expressions, in the following example where the command goes through the lines that contain either of the given arguements within the specific file

```
kevinpantoja@Kevins-MacBook-Air-5 media % grep -E "law" *.txt 
5_Legal_Groups.txt:from Utah lawyers and foundations, was the first joint fund-raising
5_Legal_Groups.txt:service law groups.
AP_LawSchoolDebts.txt:WASHINGTON (AP) - Most new lawyers won't consider working for
AP_LawSchoolDebts.txt:lawyer, prevents 66 percent of law students from taking public
AP_LawSchoolDebts.txt:"The bottom line is America's law school graduates are drowning
AP_LawSchoolDebts.txt:More than 94 percent of law students reported borrowing money to
AP_LawSchoolDebts.txt:attend law school, where median tuition is nearly $23,000 a year,
AP_LawSchoolDebts.txt:but law students are not alone in having to contend with spiraling
---SEVERAL OTHER LINES---
```

>  Another Example :

In this example, the command is used to change the patterns as the extended regular expersions, while searching for both the given arugements, which in this case is `"law|police"`.

```
kevinpantoja@Kevins-MacBook-Air-5 media % grep -E "law|police" *.txt
5_Legal_Groups.txt:from Utah lawyers and foundations, was the first joint fund-raising
5_Legal_Groups.txt:service law groups.
AP_LawSchoolDebts.txt:WASHINGTON (AP) - Most new lawyers won't consider working for
AP_LawSchoolDebts.txt:lawyer, prevents 66 percent of law students from taking public
AP_LawSchoolDebts.txt:"The bottom line is America's law school graduates are drowning
AP_LawSchoolDebts.txt:More than 94 percent of law students reported borrowing money to
---SEVERAL OTHER LINES---
```

> Example Command 4 :

`grep` has the command `-C`, which is used to print the lines and a certain ammount of lines after and before the result of the searched lines. In the followingn example it can be seen that when given the values `3 "law" Few_who_need.txt`, the code prints out the lines with a bit of context using the first arugement to give a ceratin amount of lines before and after.

```
kevinpantoja@Kevins-MacBook-Air-5 media % grep -C 3  "law" Few_who_need.txt
employment, grandparent guardianships, bankruptcy and consumer
debt, veterans' issues, elder abuse and home equity fraud, the
report said.
To meet all those needs, there is only one legal aid lawyer for
every 10,000 poor Californians. Despite this bleak picture, the
state's civil justice community has taken significant steps to
close the gap between need and services in the past five years:
--
than 100 local legal services programs.
Access to the courts has been enhanced through a variety of
self-help options, including online assistance in every county, a
system of family law facilitators, increased funding for
alternative dispute resolution and simplified forms and
procedures.
The Judicial Council is addressing language barriers by
--
report.
"More than anyone, they know it can be nearly impossible to do
the former and avoid the latter in a one-sided contest where only
one litigant has a lawyer."
"Our whole society is harmed when access and fairness are
denied," said Londen. "Clearly, California can - and must - do
better."
```

> Another Example:

In the next example we used the same command but this time we search for lines with the word `few` and gives the context of 2 lines before and after in the same file.

```
kevinpantoja@Kevins-MacBook-Air-5 media % grep -C 2  "few" Few_who_need.txt
The 1996 welfare reform legisla tion, in particular, brought
dramatic changes to the lives of those living in poverty, for while
fewer people now receive welfare benefits, those who left welfare
to work are still poor. And the legal issues they face "have become
more numerous and complex," the report said.
```
