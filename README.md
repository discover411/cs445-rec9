# CS 445 Recitation 9: List ADT

## Introduction

In this lab, you will implement the List ADT by implementing both a singly LinkedList and a double LinkedList.
The primary goal is to practice implementing the List ADT using a linked-based approach and comparing the differences between a singly and doubly linked approach.
Recall that the List ADT:
- Is ordered
- Allows duplicates
- Allows arbitrary access to elements
- Can access elements by indexing
- Has no fixed capacity
- Grows dynamically as elements are inserted
- Allows arbitrary insertions without manual shifting
- Has no guarantee of random access (fast indexing)

## Exercise

1. Download the provided code by forking and cloning this [Recitation 9 repository](https://github.com/2217-cs445/cs445-rec9). The starting code for this exercise, as usual, is found in subdirectory `app/src/main/java/`. Navigate to this subdirectory, then into the `cs445/rec9/` package folder within it. Note the following provided Java files:

   - `ListInterface.java` contains the List ADT
   - `LinkedList.java`  contains methods for the singly LinkedList and method stubs for today's exercises
   - `DoublyLinkedList.java` contains methods for the doubly LinkedList and method stubs for today's exercises
   - `ListClient.java` contains a simple client for running both singly and doubly LinkedLists using `./gradlew run` (or `gradlew.bat run` for DOS-based systems).
   - `SingleListTest.java` contains JUnit test cases for the singly LinkedList
   - `DoubleListTest.java` contains JUnit test cases for the double LinkedList

2. Implement the following methods in `LinkedList.java` to complete the singly LinkedList implementation. 

      /**
      \* Adds a new entry to the end of this list.
      \* Entries currently in the list are unaffected. The list's size is
      \* increased by 1.
      \* @param newEntry  The object to be added as a new entry.
      */
      public void add(E newEntry)

      /**
      \* Adds a new entry at a specified position within this list.
      \* Entries originally at and above the specified position are at the next
      \* higher position within the list. The list's size is increased by 1.
      \* @param newPosition  An integer that specifies the desired position of the
      \* new entry.
      \* @param newEntry  The object to be added as a new entry.
      \* @throws  IndexOutOfBoundsException if newPosition < 0 or
      \* newPosition > getSize().
      */
      public void add(int newPosition, E newEntry)

3. Test that your methods pass the provided tests using `./gradlew test` (or `gradlew.bat test` on DOS-based terminals) and debug any errors with these two methods. 

4. Compare your implementation of both add methods in the singly LinkedList to the add methods of the doubly LinkedList in `DoublyLinkedList.java`. How are the two implementations similar? How do the two implementations differ?

5. Implement the following method in `DoublyLinkedList.java` to complete the doubly LinkedList implementation.

      /**
      \* Removes the entry at a given position from this list.
      \* Entries originally at positions higher than the given position are at the
      \* next lower position within the list, and the list's size is decreased by
      \* 1.
      \* @param position  An integer that indicates the position of the entry to
      \* be removed.
      \* @return  A reference to the removed entry.
      \* @throws  IndexOutOfBoundsException if position < 0 or
      \* position >= getSize().
      */
      public E remove(int position)

6. Test that your methods pass the provided tests using `./gradlew test` (or `gradlew.bat test` on DOS-based terminals) and debug any errors with this method. 

7. Compare your implementation of remove in the doubly LinkedList to the remove method of the singly LinkedList in `LinkedList.java`. How are the two implementations similar? How do the two implementations differ?

## Conclusion

In this exercise, you practiced implementing the List ADT using a linked-based approach in order to compare the differences between a singly LinkedList and a doubly LinkedList. Even though both implementations are linked-based and implement the List ADT, there will be different scenarios when a doubly LinkedList is optimal while unnecessary in other situations. It is important to understand how to implement an ADT, but it is also important to determine which implementation is most effective for a specific problem. 
