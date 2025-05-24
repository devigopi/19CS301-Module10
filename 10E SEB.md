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

