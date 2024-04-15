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
![Alt Text](https://github.com/Mohanrajx/Image/blob/c268a30deff0a33611d3758dd7c929bd16d24fb5/code_20240415_192205_via_10015_io.png)

##
#### 5(A) To write a Python PROGRAM to insert elements into stack.
#### PROGRAM
![Alt Text](https://github.com/Mohanrajx/Image/blob/631dceab274802abb9b41477ca8ffa383da25c1f/code_20240415_191750_via_10015_io.png)


##
#### 5(B) To write a Python PROGRAM to implement queue.
#### PROGRAM
![Alt Text](https://github.com/Mohanrajx/Image/blob/1fbe617af697642a77c3a39d6c37f08353aadfb2/code_20240415_191439_via_10015_io.png)

##
#### 6(A) To write a Python PROGRAM for card of game in Python in List ADT.
#### PROGRAM
![Alt Text](https://github.com/Mohanrajx/Image/blob/6a86536a5ade17728f54a23a57b09471c89f2691/code_20240415_190343_via_10015_io.png)

##
#### 6(B) To write a Python code for infix to postfix conversion.
#### PROGRAM
![Alt Text](https://github.com/Mohanrajx/DSD/blob/02864c920f4f2ebe4a1506e700f6f4cce70320fc/code_20240415_185752_via_10015_io.png)


##
#### 6(C). To write a Python PROGRAM for first come first serve scheduling PROGRAM.
#### PROGRAM
![Alt Text](https://github.com/Mohanrajx/DSD/blob/f8eeeb9c8e97cff48a929784159753e08150db70/code_20240415_184907_via_10015_io.png)

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
    
![Alt Text](https://github.com/Mohanrajx/Image/blob/2a59539071a38fd33b14bd288ea21f24ad72f11a/code_20240415_192603_via_10015_io.png)
   
</details>

#### EASIEST VERSION OF CODE
![Alt Text](https://github.com/Mohanrajx/Image/blob/c14efe9ec99c8c01174a9fa3459ea761e1d0f58b/code_20240415_193149_via_10015_io.png)

##
### I shall expeditiously conclude the outstanding updates.
##
# GM 



