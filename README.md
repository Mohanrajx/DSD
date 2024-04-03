# DSD PROGRAM 
#### 1(A) Write a Python PROGRAM to calculate electricity bill for a given tariff.

• 1 to 100 units – Rs. 10

• 100 to 200 units – Rs. 15

• 200 to 300 units – Rs.20

• above 300 units – Rs. 25
###### PROGRAM
```
units = int(input("Enter the number of units consumed:"))

billamount = units * 10 if units <= 100 else (1000 + (units - 100) * 15) if units <= 200 else (2500 + (units - 200) * 20) if units <= 300 else (4500 + (units - 300) * 25)

print(f"The electricity bill for {units} units is Rs. {billamount}")
```
##
#### 1(B) To write a Python PROGRAM for basic operations of calculator.
#### PROGRAM
```
from abc import ABC, abstractmethod

class Operation(ABC):

    @abstractmethod
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
    element = int(input("Enter an element: "))
    arr_list.append(element)
element_to_search = int(input("Enter the element to search: "))
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
    head = Node(int(input("Enter data item: ")))
    current = head
    for _ in range(n - 1):
        current.next = Node(int(input("Enter data item: ")))
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
        while current:
            if current.data == key:
                return True
            current = current.next
        return False

llist = LinkedList()
for _ in range(int(input("Enter the number of elements in the linked list: "))):
    llist.append(int(input("Enter an element: ")))

key = int(input("Enter the element to search: "))
print(f"Key element {key} found in the linked list" if llist.search(key) else f"Key element {key} not found in the linked list")
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

    def display(self):
        print("Stack:", self.stack)

stack = Stack()

while True:
    element = input("Enter element (or 'done' to stop): ")
    if element.lower() == 'done':
        break
    stack.push(element)
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

# Example usage with user input
while True:
    value = input("Enter a value to enqueue (or 'done' to stop): ")
    if value.lower() == 'done':
        break
    enqueue(value)

display()

if not is_empty():
    print("After removing an element")
    dequeue()
    display()
else:
    print("Queue is empty")

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
# G.M 
