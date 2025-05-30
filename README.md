# 19CS301-Module10
###EX: 10.a  STACK
### Aim: To Write a python program to get the integer values from the user and push only the odd number into the stack and later pop the last 2 elements
### Algorithm:
STEP 1: Start.

STEP 2: Create a list and a variable n.

STEP 3: Get the value of n from user.

STEP 4: Using loop append only odd elements in the stack.

STEP 5 : Using another loop using built-in pop operation pop the last two elements.

STEP 6: Print the result.

STEP 7 : Stop.
### Program:
```
l = []
n = int(input())
for i in range(n):
       x = int(input())
       if x%2!=0:
            l.append(x)
 print(l)
for i in range(2):
      l.pop()
     print(l)
```
### Output:
 ![image](https://github.com/user-attachments/assets/d2ce0434-7594-41af-ba20-3d7ecf9e0d93)

### Result: Thus, the given program is implemented and executed successfully .
 


### EX: 10.2 IMPLEMENTATION OF STACK
### Aim: To Write a python program to implement the stack using deque method for rotating the stack.
### Algorithm:

STEP 1: Start.

STEP 2: Import collections and import deque.

STEP 3: Create a list and get the input from user.

STEP 4: Create a variable n and get number of inputs from user.

STEP 5 : Using a loop get the inputs from user and append in deque.

STEP 6: Using rotate function rotate the stack.

STEP 7 : Print the result. 

STEP 8 : Stop.
### Program: 
```
import collections
def fun(n):
   stack = collections.deque([])
   a=int(input())
   for i in range (a):
         x=stack.append(int(input()))
     print(f"Stack before rotation {stack}") stack.rotate(n)
print(f"Stack after rotation {stack}")
```
### Output:
![image](https://github.com/user-attachments/assets/f42c4ec6-578c-418a-8f66-cf70abe7dc54)

### Result: Thus, the given program is implemented and executed successfully .
 


EX: 10.3 QUEUE
### Aim: To Write a develop a python program to remove the last 3 values from the queue 
### Algorithm:

STEP 1: Start.
STEP 2:Initialize a queue (FIFO) — use collections.deque for efficient operations.
STEP 3:Check if the queue has at least 3 elements:
       If yes, repeat 3 times:
       Use .pop() to remove the last (rightmost) element.
       If no, clear the entire queue using .clear().
STEP 4:Display the modified queue.
STEP 5:End

### Program:
```
from collections import deque
que = []  
n=int(input())
for i in range(n):
    que.append(int(input()))  
for i in range(3):
    que.pop()
print(que)
```
### Output:

 ![10 A](https://github.com/user-attachments/assets/0dfb96a4-ccdb-451b-acd6-e7772d9ac130)

### Result: Thus, the given program is implemented and executed successfully .


### EX: 10.4 IMPLEMENTATION OF QUEUE
### Aim: To Develop a python program to get the 4 integer values from user and display the values using multiprocessing library
### Algorithm:

STEP 1: Start.

STEP 2: From Multiprocessing Import Queue.

STEP 3: Create a list and get the input from user.

STEP 4 : Append the elements in the list.

STEP 5: Using 'get' built-in function print the list.

STEP 6 : Print the result.

STEP 7 : Stop.
### Program:
```
from multiprocessing import Queue
queue = Queue()
for i in range(4):
    queue.put(int(input()))
for i in range(4):
     print(queue.get())
```
### Output:
 ![image](https://github.com/user-attachments/assets/26a380ff-118e-43f4-8178-83a5417262b5)
 

### Result: Thus, the given program is implemented and executed successfully .

10E EX: Circular queue

Aim:
    Develop a python program to remove 3 values from the user and display the values using circular queue

Algorithm:
Step 1:Start
Step 2:Define the maximum size (MAX) of the circular queue.
Step 3:Create a list (queue) to store elements and initialize front and rear pointers.
Step 4:Input values into the circular queue until it is full.
Step 5:Define a dequeue() function:
    If the queue is empty, return a message.
    Else remove the front element, update the front pointer circularly.
Step 6:Call dequeue() 3 times to remove the first 3 elements.
Step 7:Display the remaining elements in the circular queue using the current positions of front and rear.
Step 8:End

Program:
```
class MyCircularQueue():
    def __init__(self, k):
        self.k = k
        self.queue = [None] * k
        self.head = self.tail = -1
    def enqueue(self, data):
        if ((self.tail + 1) % self.k == self.head):
            print("The circular queue is full\n")
        elif (self.head == -1):
            self.head = 0
            self.tail = 0
            self.queue[self.tail] = data
        else:
            self.tail = (self.tail + 1) % self.k
            self.queue[self.tail] = data
    def dequeue(self):
        if(self.head==-1):
            print("The circular queue is empty\n")
        elif(self.head==self.tail):
            temp=self.queue[self.head]
            self.head=-1
            self.tail=-1
            return temp
        else:
            temp=self.queue[self.head]
            self.head=(self.head+1)%self.k
            return temp
 
    def printCQueue(self):
        if(self.head==-1):
            print("No element in the circular queue")
        elif(self.tail>=self.head):
            for i in range(self.head,self.tail+1):
                print(self.queue[i],end=" ")
            print()
        else:
            for i in range(self.head,self.k):
                print(self.queue[i],end=" ")
            for i in range (0,self.tail+1):
                print(self.queue[i],end=" ")
            print()
obj = MyCircularQueue(5)
for i in range(5):
    obj.enqueue(int(input()))
obj.dequeue()
obj.dequeue()
obj.dequeue()
obj.printCQueue()
```
Output:
![10e](https://github.com/user-attachments/assets/b82e7b2c-9d1d-4bd4-bbba-bf642d77c588)

Result:
    Thus, the given program is implemented and executed successfully .
 

