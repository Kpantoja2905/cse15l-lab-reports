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

The command that I want to explore is `grep`


