# DSD PROGRAM 
#####

---

**Disclaimer:**

<sup>These programs are for reference only. Do not copy them for use in assignments or labs, including the Data Structures Design (DSD) lab. Use them for learning and develop your own solutions independently. The author is not responsible for any misuse.</sup>

---
#### 1(A) Write a Python PROGRAM to calculate electricity bill for a given tariff.

• 1 to 100 units – Rs. 10

• 100 to 200 units – Rs. 15

• 200 to 300 units – Rs.20

• above 300 units – Rs. 25
#### PROGRAM
```
units = float(input("Enter the number of units consumed:"))

billamount = units * 10 if units <= 100 else (1000 + (units - 100) * 15) if units <= 200 else (2500 + (units - 200) * 20) if units <= 300 else (4500 + (units - 300) * 25)

print(f"The electricity bill for {units} units is Rs. {billamount}")
```
##
#### 1(B) To write a Python PROGRAM for basic operations of calculator.
#### PROGRAM
```
from abc import ABC, abstractmethod

class Operation(ABC):

    def operate(self, a, b):
        pass

class Addition(Operation):

    def operate(self, a, b):
        return a + b

class Subtraction(Operation):

    def operate(self, a, b):
        return a - b

class Multiplication(Operation):

    def operate(self, a, b):
        return a * b

class Division(Operation):

    def operate(self, a, b):
        if b != 0:
            return a / b
        else:
            return "Cannot divide by zero"

a = float(input("Enter the first number: "))
b = float(input("Enter the second number: "))

addition = Addition()
print("Addition:", addition.operate(a, b))

subtraction = Subtraction()
print("Subtraction:", subtraction.operate(a, b))

multiplication = Multiplication()
print("Multiplication:", multiplication.operate(a, b))

division = Division()
print("Division:", division.operate(a, b))
```
##
#### 2(A) Write a Python PROGRAM to find factorial calculation using recursion.
#### PROGRAM
```
def factorial(n):
    return 1 if n == 0 else n * factorial(n - 1)

num = int(input("Enter a number: "))
print("Factorial of", num, "is", factorial(num))
```
##
#### 2(B) To write a Python PROGRAM for Tower of Hanoi using recursion.
#### PROGRAM
```
def tower_of_hanoi(n, source, target, auxiliary):
    if n == 1:
        print(f"Move disk 1 from {source} to {target}")
        return
    tower_of_hanoi(n - 1, source, auxiliary, target)
    print(f"Move disk {n} from {source} to {target}")
    tower_of_hanoi(n - 1, auxiliary, target, source)
n = int(input("Enter the number of disks: "))
tower_of_hanoi(n, 'A', 'C', 'B')

```
##
#### 3(A) To write a Python PROGRAM to search element in a list using arrays.
#### PROGRAM
```
class ArrayList:
    def __init__(self):
        self.array = []
    def append(self, element):
        self.array.append(element)
    def search(self, element):
        for i in range(len(self.array)):
            if self.array[i] == element:
                return True, i
        return False, -1
arr_list = ArrayList()
n = int(input("Enter the number of elements in the list: "))
for _ in range(n):
    element = float(input("Enter an element: "))
    arr_list.append(element)
element_to_search = float(input("Enter the element to search: "))
found, index = arr_list.search(element_to_search)
if found:
    print(f"Element {element_to_search} found at index {index}")
else:
    print(f"Element {element_to_search} not found")

```
##
#### 4(A) To write a Python PROGRAM to create linked list with n elements.
#### PROGRAM
```
class Node:
    def __init__(self, data=None):
        self.data = data
        self.next = None

def create_linked_list():
    n = int(input("How many elements would you like to add? "))
    if n <= 0:
        return None
    head = Node(float(input("Enter data item: ")))
    current = head
    for _ in range(n - 1):
        current.next = Node(float(input("Enter data item: ")))
        current = current.next
    return head

def display_linked_list(head):
    current = head
    while current:
        print(current.data, end=" ")
        current = current.next
    print()

head = create_linked_list()
print("The linked list:", end=" ")
display_linked_list(head)
```
##
#### 4(B) To write a Python PROGRAM to search key element in a linked list.
#### PROGRAM
```
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
class LinkedList:
    def __init__(self):
        self.head = None
    def append(self, data):
        new_node = Node(data)
        if self.head is None:
            self.head = new_node
            return
        last_node = self.head
        while last_node.next:
            last_node = last_node.next
        last_node.next = new_node
    def search(self, key):
        current = self.head
        index = 0
        while current:
            if current.data == key:
                return True, index
            current = current.next
            index += 1
        return False, -1
llist = LinkedList()
for _ in range(int(input("Enter the number of elements in the linked list: "))):
    llist.append(float(input("Enter an element: ")))
key = float(input("Enter the element to search: "))
found, index = llist.search(key)
if found:
    print(f"Key element {key} found at index {index} in the linked list")
else:
    print(f"Key element {key} not found in the linked list")

```
##
#### 5(A) To write a Python PROGRAM to insert elements into stack.
#### PROGRAM
```
class Stack:
    def __init__(self):
        self.stack = []

    def push(self, element):
        self.stack.append(element)
        self.display()

    def pop(self, element=None):
        if element is None:
            if not self.is_empty():
                self.stack.pop()
                self.display()
            else:
                print("Stack is empty")
        else:
            try:
                self.stack.remove(element)
                self.display()
            except ValueError:
                print(f"Element '{element}' not found in the stack")

    def is_empty(self):
        return len(self.stack) == 0

    def display(self):
        print("Stack:", self.stack)

stack = Stack()

while True:
    action = input("Enter action (push/pop/done): ")
    if action.lower() == 'done':
        break
    elif action.lower() == 'push':
        element = input("Enter element to push: ")
        stack.push(element)
    elif action.lower() == 'pop':
        element = input("Enter element to pop (leave blank to pop the top element): ")
        stack.pop(element if element else None)
    else:
        print("Invalid action. Please enter 'push', 'pop', or 'done'")

```
##
#### 5(B) To write a Python PROGRAM to implement queue.
#### PROGRAM
```
queue = []

def enqueue(item):
    queue.append(item)

def dequeue():
    if not is_empty():
        return queue.pop(0)
    else:
        raise IndexError("dequeue from empty queue")

def is_empty():
    return not queue

def size():
    return len(queue)

def display():
    print("Queue:", queue)

def remove_element(element):
    if element in queue:
        queue.remove(element)
        print(f"Element '{element}' removed from the queue")
    else:
        print(f"Element '{element}' not found in the queue")
while True:
    action = input("Enter 'enqueue' to add an item, 'remove' to remove a specific element, or 'done' to stop: ")
    if action.lower() == 'done':
        break
    elif action.lower() == 'enqueue':
        value = input("Enter a value to enqueue: ")
        enqueue(value)
        display()
    elif action.lower() == 'remove':
        element_to_remove = input("Enter the element to remove from the queue: ")
        remove_element(element_to_remove)
        display()
    else:
        print("Invalid action")
display()
print("Size:", size())
print("Is empty:", is_empty())

```
##
#### 6(A) To write a Python PROGRAM for card of game in Python in List ADT.
#### PROGRAM
```
import random

suits = ['Hearts', 'Diamonds', 'Clubs', 'Spades']
ranks = ['2', '3', '4', '5', '6', '7', '8', '9', '10', 'Jack', 'Queen', 'King', 'Ace']
deck = [(rank, suit) for suit in suits for rank in ranks]
random.shuffle(deck)

def deal_hand(num_cards):
    return [deck.pop() for _ in range(num_cards)]

def display_hand(player, hand):
    print(f"{player}'s hand:")
    for card in hand:
        print(f"{card[0]} of {card[1]}")

def determine_winner(player_hand, computer_hand):
    player_ranks = [ranks.index(card[0]) for card in player_hand]
    computer_ranks = [ranks.index(card[0]) for card in computer_hand]
    player_score = sum(player_ranks)
    computer_score = sum(computer_ranks)
    if player_score > computer_score:
        return "You win!"
    elif player_score < computer_score:
        return "You lose!"
    else:
        return "It's a tie!"

player_hand = deal_hand(5)
computer_hand = deal_hand(5)

display_hand("Your", player_hand)
display_hand("Computer's", computer_hand)

print(determine_winner(player_hand, computer_hand))
```
##
#### 6(B) To write a Python code for infix to postfix conversion.
#### PROGRAM
```
def infix_to_postfix(expression):
    precedence = {'+': 1, '-': 1, '*': 2, '/': 2, '^': 3}
    stack = []
    postfix = []
    
    for char in expression:
        if char.isalnum():
            postfix.append(char)
        elif char == '(':
            stack.append(char)
        elif char == ')':
            while stack and stack[-1] != '(':
                postfix.append(stack.pop())
            stack.pop()  # Discard the '('
        else:  # Operator
            while stack and precedence.get(stack[-1], 0) >= precedence.get(char, 0):
                postfix.append(stack.pop())
            stack.append(char)

    while stack:
        postfix.append(stack.pop())

    return ''.join(postfix)

# Get input from user
infix_expression = input("Enter an infix expression: ")

# Display infix expression
print("Infix expression:", infix_expression)

# Convert infix to postfix and display the result
postfix_expression = infix_to_postfix(infix_expression)
print("Postfix expression:", postfix_expression)
```
##
#### 6(C). To write a Python PROGRAM for first come first serve scheduling PROGRAM.
#### PROGRAM
```
def fcfs(processes):
    # Initialize variables
    total_waiting_time = 0
    total_turnaround_time = 0

    # Set initial values for the first process
    current_time = 0

    # Process and print each process
    print("Process\tArrival Time\tBurst Time\tWaiting Time\tTurnaround Time")
    for process in processes:
        # Calculate waiting time
        waiting_time = max(0, current_time - process[1])

        # Calculate turnaround time
        turnaround_time = waiting_time + process[2]

        # Update total waiting and turnaround times
        total_waiting_time += waiting_time
        total_turnaround_time += turnaround_time

        # Update current time
        current_time += process[2]

        # Print process details
        print(f"{process[0]}\t{process[1]}\t\t{process[2]}\t\t{waiting_time}\t\t{turnaround_time}")

    # Calculate average waiting and turnaround times
    n = len(processes)
    avg_waiting_time = total_waiting_time / n
    avg_turnaround_time = total_turnaround_time / n

    # Print average times
    print(f"\nAverage Waiting Time: {avg_waiting_time}")
    print(f"Average Turnaround Time: {avg_turnaround_time}")

# Input process details
if __name__ == "__main__":
    n = int(input("Enter the number of processes: "))
    processes = []
    for i in range(1, n + 1):
        arrival_time = float(input(f"Enter arrival time for process {i}: "))
        burst_time = float(input(f"Enter burst time for process {i}: "))
        processes.append((i, arrival_time, burst_time))
    
    fcfs(processes)
```
##
#### 7(A) To write a Python script for implementing linear search technique.
#### PROGRAM
```
def linear_search(arr, x):
    for i in range(len(arr)):
        if arr[i] == x:
            return i  
    return -1  
arr = []
n = int(input("Enter the number of elements in the list: "))
for _ in range(n):
    element = float(input("Enter element: "))
    arr.append(element)
x = float(input("Enter the element to search for: "))
result = linear_search(arr, x)

if result != -1:
    print(f"Element found at index {result}")
else:
    print("Element not found")
```
##
#### 7(B) IMPLEMENTATION OF BINARY SEARCHING TECHNIQUE
###### Write a Python PROGRAM to search an element in a given linear list using recursion 
#### PROGRAM
```
def binary_search(arr, low, high, x):
    if high >= low:
        mid = low + (high - low) // 2
        if arr[mid] == x:
            return mid
        elif arr[mid] > x:
            return binary_search(arr, low, mid - 1, x)
        else:
            return binary_search(arr, mid + 1, high, x)
    else:
        return -1
arr = []
n = int(input("Enter the number of elements in the sorted list: "))
for _ in range(n):
    element = float(input("Enter element: "))
    arr.append(element)
arr.sort()
x = float(input("Enter the element to search for: "))
result = binary_search(arr, 0, len(arr) - 1, x)

if result != -1:
    print(f"Element found at index {result}")
else:
    print("Element not found")
```
##
#### 7(C) To write a Python PROGRAM to arrange the given elements using bubble sort.
#### PROGRAM
```
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
arr = list(map(float, input("Enter elements of the list separated by spaces: ").split()))
bubble_sort(arr)
print("Sorted list:", arr)
```
##
#### 7(D) To write a Python PROGRAM to arrange the given elements using insertion sort.
#### PROGRAM
```
def insertion_sort(arr):
    for i in range(1, len(arr)):
        key = arr[i]
        j = i - 1
        while j >= 0 and key < arr[j]:
            arr[j + 1] = arr[j]
            j -= 1
        arr[j + 1] = key

n = int(input("Enter the number of elements: "))
arr = []
for _ in range(n):
    element = float(input("Enter element: "))
    arr.append(element)

insertion_sort(arr)

print("Sorted array is:", arr)
```
##
#### 7(E) To write a Python PROGRAM to arrange the given elements using selection sort.
#### PROGRAM
```
def selection_sort(arr):
    n = len(arr)
    for i in range(n):
        min_idx = i
        for j in range(i+1, n):
            if arr[j] < arr[min_idx]:
                min_idx = j
        arr[i], arr[min_idx] = arr[min_idx], arr[i]
    return arr

arr = input("Enter the elements separated by spaces: ").split()
arr = [float(num) for num in arr]

sorted_arr = selection_sort(arr)
print("Sorted array is:", sorted_arr)
```
##
#### 8(A) To write a Python PROGRAM to print a binary tree in vertical order.
#### PROGRAM

![Alt Text](https://github.com/Mohanrajx/DSD/blob/bff99ac3409dd91fbb26ba7bcb630e10d55d75c8/Mohanrajx9A.png)

<details>
  <summary><h4>Sample Output for 8A</h4></summary>
 
 ```
Enter the value of the root node: 1
Enter the value of the left child of root (or 'None' if no left child): 2
Enter the value of the right child of root (or 'None' if no right child): 3
Enter the value of the left child of left child of 1 (or 'None' if no left child): 4
Enter the value of the right child of left child of 1 (or 'None' if no right child): 5
Enter the value of the left child of right child of 1 (or 'None' if no left child): none
Enter the value of the right child of right child of 1 (or 'None' if no right child): 6
Enter the value of the left child of left child of 2 (or 'None' if no left child): None
Enter the value of the right child of left child of 2 (or 'None' if no right child): none
Enter the value of the left child of right child of 2 (or 'None' if no left child): none
Enter the value of the right child of right child of 2 (or 'None' if no right child): None
Enter the value of the left child of right child of 3 (or 'None' if no left child): none
Enter the value of the right child of right child of 3 (or 'None' if no right child): NoNe
Vertical order traversal of binary tree is:
4
2
1 5
3
6
```
</details>

##
#### 9A. To write a Python PROGRAM in order to traverse and search element from binary tree 🌲 .
### PROGRAM

<details>
  <summary><h5>74 lines of code</h5></summary>

```
class Node:
    def __init__(self, key):
        self.left = None
        self.right = None
        self.val = key
        self.index = None

def inorder_traversal(root):
    if root:
        inorder_traversal(root.left)
        print(f"{root.val} at position {root.index}", end=" ")
        inorder_traversal(root.right)

def preorder_traversal(root):
    if root:
        print(f"{root.val} at position {root.index}", end=" ")
        preorder_traversal(root.left)
        preorder_traversal(root.right)

def postorder_traversal(root):
    if root:
        postorder_traversal(root.left)
        postorder_traversal(root.right)
        print(f"{root.val} at position {root.index}", end=" ")

def search_element(root, key, index=1):
    if root is None or root.val == key:
        if root:
            root.index = index
        return root

    if root.val < key:
        return search_element(root.right, key, 2 * index + 1)

    return search_element(root.left, key, 2 * index)

# Function to insert a new node with the given key
def insert_node(root, key):
    if root is None:
        return Node(key)
    else:
        if key < root.val:
            root.left = insert_node(root.left, key)
        else:
            root.right = insert_node(root.right, key)
    return root

# Get user input to build the binary tree
def build_binary_tree():
    root = None
    elements = []
    n = int(input("Enter the number of elements in the binary tree: "))
    print("Enter the elements:",)
    for _ in range(n):
        key = float(input())
        elements.append(key)
        root = insert_node(root, key)
    print("Elements entered:", elements)
    return root
root = build_binary_tree()

print("\nInorder traversal:")
inorder_traversal(root)
print("\nPreorder traversal:")
preorder_traversal(root)
print("\nPostorder traversal:")
postorder_traversal(root)

key = float(input("\nEnter the element to search in the tree: "))
result = search_element(root, key)
if result:
    print(f"Element {key} found in the tree at position {result.index}.")
else:
    print(f"Element {key} not found in the tree.")
    
```
</details>

#### EASIEST VERSION OF CODE
```
class Node:
    def __init__(self, key):
        self.left = None
        self.right = None
        self.val = key
        self.index = None

def traverse(root, order=lambda r: (root := r) and traverse(r.left) + [r.val] + traverse(r.right) if r else []):
    return order(root)

def search(root, key, index=1):
    if not root or root.val == key: root and setattr(root, 'index', index)
    return root if not root or root.val == key else search(root.right, key, 2 * index + 1) if root.val < key else search(root.left, key, 2 * index)

def insert(root, key):
    return Node(key) if not root else (setattr(root, 'left', insert(root.left, key)) if key < root.val else setattr(root, 'right', insert(root.right, key)), root)[1]

def build_tree():
    root, elements = None, []
    for _ in range(int(input("Enter the number of elements in the binary tree: "))): elements.append(float(input())) ; root = insert(root, elements[-1])
    print("Elements entered:", elements)
    return root

root = build_tree()
print("\nInorder traversal:", traverse(root))
print("Preorder traversal:", traverse(root, lambda r: [r.val] + traverse(r.left) + traverse(r.right)))
print("Postorder traversal:", traverse(root, lambda r: traverse(r.left) + traverse(r.right) + [r.val]))

key = float(input("\nEnter the element to search in the tree: "))
result = search(root, key)
print(f"Element {key} found in the tree at position {result.index}." if result else f"Element {key} not found in the tree.")
```
##
### I shall expeditiously conclude the outstanding updates.
##
# GM 



