# The site has been permanently deleted by the admin due to high levels of unethical behavior. If there is a genuine need for educational purposes, please feel free to contact the admin.


#### Priority queue
#### program 
```
import heapq

class PriorityQueue:
    def __init__(self):
        self._queue = []
        self._index = 0

    def push(self, item, priority):
        heapq.heappush(self._queue, (-priority, self._index, item))
        self._index += 1

    def pop(self):
        return heapq.heappop(self._queue)[-1]

    def is_empty(self):
        return len(self._queue) == 0

# Create a PriorityQueue instance
pq = PriorityQueue()

# Get input from the user for tasks and priorities
while True:
    task = input("Enter the task (or type 'done' to finish): ")
    if task.lower() == 'done':
        break
    priority = int(input("Enter the priority for the task: "))
    pq.push(task, priority)

# Pop and print tasks with highest priority
print("\nTasks in priority order:")
while not pq.is_empty():
    print(pq.pop())

```

#### Output
```
Enter the task (or type 'done' to finish): Study
Enter the priority for the task: 3
Enter the task (or type 'done' to finish): Exercise
Enter the priority for the task: 2
Enter the task (or type 'done' to finish): Read
Enter the priority for the task: 1
Enter the task (or type 'done' to finish): done

Tasks in priority order:
Study
Exercise
Read
```
#### Topic : Implementation of Hash Map
#### program 
```
# Initialize an empty hash map
hash_map = {}

# Get user choice
choice = input("Enter 'a' to add a key-value pair, 'g' to get a value by key, or 'q' to quit: ")

# Process user choice
while choice != 'q':
    if choice == 'a':
        key = input("Enter key: ")
        value = input("Enter value: ")
        hash_map[key] = value
    elif choice == 'g':
        key = input("Enter key to get value: ")
        if key in hash_map:
            print("Value:", hash_map[key])
        else:
            print("Key not found")
    else:
        print("Invalid choice")

    # Get next choice
    choice = input("Enter 'a' to add a key-value pair, 'g' to get a value by key, or 'q' to quit: ")

```

#### output 
```

Enter 'a' to add a key-value pair, 'g' to get a value by key, or 'q' to quit: a
Enter key: name
Enter value: Hello World
Enter 'a' to add a key-value pair, 'g' to get a value by key, or 'q' to quit: a
Enter key: age
Enter value: 24
Enter 'a' to add a key-value pair, 'g' to get a value by key, or 'q' to quit: g
Enter key to get value: name
Value: Hello World 
Enter 'a' to add a key-value pair, 'g' to get a value by key, or 'q' to quit: g
Enter key to get value: gender
Key not found
Enter 'a' to add a key-value pair, 'g' to get a value by key, or 'q' to quit: q

```



### Mine

```
Enter the number of elements: 20
Enter element 1: 833883
Enter element 2: 8388
Enter element 3: 838
Enter element 4: 883
Enter element 5: 321
Enter element 6: 213
Enter element 7: 97
Enter element 8: 183
Enter element 9: 088
Enter element 10: 472
Enter element 11: 61
Enter element 12: 421
Enter element 13: 8
Enter element 14: 7
Enter element 15: 6
Enter element 16: 5
Enter element 17: 4
Enter element 18: 3
Enter element 19: 2
Enter element 20: 1
Bubble Sort Time: 0.0012180805206298828
Selection Sort Time: 0.000522613525390625
Merge Sort Time: 0.0009989738464355469
Quick Sort Time: 0.0006504058837890625

```
