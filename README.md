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
![Alt Text](https://github.com/Mohanrajx/Image/blob/a15ee04334bcbf4c966f30723dfde5a194cd8aa9/code_20240415_222930_via_10015_io.png)
```
units = float(input("Enter the number of units consumed:"))

billamount = units * 10 if units <= 100 else (1000 + (units - 100) * 15) if units <= 200 else (2500 + (units - 200) * 20) if units <= 300 else (4500 + (units - 300) * 25)

print(f"The electricity bill for {units} units is Rs. {billamount}")
```
##
<details>
<summary>
Sample Output :
</summary>

![Alt Text](https://github.com/Mohanrajx/Image/blob/6269248e61043c9e5cf7647b523267ada2a8b0e9/code_20240419_131456_via_10015_io.png)


</details>

---
#### 1(B) To write a Python PROGRAM for basic operations of calculator.
#### PROGRAM
![Alt Text](https://github.com/Mohanrajx/Image/blob/5a3d4a58b469dd38398737a8dcd9c46fa4472765/code_20240415_223533_via_10015_io.png)

##
<details>
<summary>
Sample Output :
</summary>

![Alt Text](https://github.com/Mohanrajx/Image/blob/e742342adeadd5f1ee62a5a4af6a754c3497dcb4/code_20240419_131256_via_10015_io.png)


</details>

---
#### 2(A) Write a Python PROGRAM to find factorial calculation using recursion.
#### PROGRAM
![Alt Text](https://github.com/Mohanrajx/Image/blob/cc888af614df60a07eec37b8db67770bf02df2aa/code_20240415_224006_via_10015_io.png)
##
<details>
<summary>
Sample Output :
</summary>

![Alt Text](https://github.com/Mohanrajx/Image/blob/f4612d092946ae041a57c93bd7c25ecc0d4edbdb/code_20240419_131109_via_10015_io.png)


</details>

---
#### 2(B) To write a Python PROGRAM for Tower of Hanoi using recursion.
#### PROGRAM
![Alt Text](https://github.com/Mohanrajx/Image/blob/963a42b81347c01997890c9654dbc948a4251fac/code_20240415_224457_via_10015_io.png)
##
<details>
<summary>
Sample Output :
</summary>

![Alt Text](https://github.com/Mohanrajx/Image/blob/f315b27d9351cc1191414da4ad3d3c49dd3b0d7e/code_20240419_130901_via_10015_io.png)


</details>

---
#### 3(A) To write a Python PROGRAM to search element in a list using arrays.
#### PROGRAM
![Alt Text](https://github.com/Mohanrajx/Image/blob/4e145c966b3f1e97f3ec812c564cf6fa2fff2970/code_20240415_224857_via_10015_io.png)
##
<details>
<summary>
Sample Output :
</summary>

![Alt Text](https://github.com/Mohanrajx/Image/blob/0f5f6dcb9f0e9cc214ee41d448b89cacdc58a6a9/code_20240419_130630_via_10015_io.png)


</details>

---
#### 4(A) To write a Python PROGRAM to create linked list with n elements.
#### PROGRAM
![Alt Text](https://github.com/Mohanrajx/Image/blob/9b8c68af9c2bde20ed007c76f3b7f163f1e7845f/code_20240415_225214_via_10015_io.png)

##
<details>
<summary>
Sample Output :
</summary>

![Alt Text](https://github.com/Mohanrajx/Image/blob/980f658192ee4e94691ceb8f8092acd243b6f214/code_20240419_130419_via_10015_io.png)


</details>

---
#### 4(B) To write a Python PROGRAM to search key element in a linked list.
#### PROGRAM
![Alt Text](https://github.com/Mohanrajx/Image/blob/c268a30deff0a33611d3758dd7c929bd16d24fb5/code_20240415_192205_via_10015_io.png)

##
<details>
<summary>
Sample Output :
</summary>

![Alt Text](https://github.com/Mohanrajx/Image/blob/0d6a1f5b5b13bd9383de7f0d57c5a13494e8e285/code_20240419_130217_via_10015_io.png)


</details>

---
#### 5(A) To write a Python PROGRAM to insert elements into stack.
#### PROGRAM
![Alt Text](https://github.com/Mohanrajx/Image/blob/631dceab274802abb9b41477ca8ffa383da25c1f/code_20240415_191750_via_10015_io.png)

##
<details>
<summary>
Sample Output :
</summary>

![Alt Text](https://github.com/Mohanrajx/Image/blob/3265f26616e41b0566440d7fed09821c535f9f77/code_20240419_125957_via_10015_io.png)


</details>

---
#### 5(B) To write a Python PROGRAM to implement queue.
#### PROGRAM
![Alt Text](https://github.com/Mohanrajx/Image/blob/1fbe617af697642a77c3a39d6c37f08353aadfb2/code_20240415_191439_via_10015_io.png)

##
<details>
<summary>
Sample Output :
</summary>

![Alt Text](https://github.com/Mohanrajx/Image/blob/198a664cabfb60ac94655947437c39e0f460b866/code_20240419_125652_via_10015_io.png)


</details>

---
#### 6(A) To write a Python PROGRAM for card of game in Python in List ADT.
#### PROGRAM
![Alt Text](https://github.com/Mohanrajx/Image/blob/6a86536a5ade17728f54a23a57b09471c89f2691/code_20240415_190343_via_10015_io.png)

##
<details>
<summary>
Sample Output :
</summary>

![Alt Text](https://github.com/Mohanrajx/Image/blob/2b2eadd9d7e9d8a4ac9e51decd1501b8e2a98d8e/code_20240419_125407_via_10015_io.png)


</details>

---
#### 6(B) To write a Python code for infix to postfix conversion.
#### PROGRAM
![Alt Text](https://github.com/Mohanrajx/DSD/blob/02864c920f4f2ebe4a1506e700f6f4cce70320fc/code_20240415_185752_via_10015_io.png)

##
<details>
<summary>
Sample Output :
</summary>

![Alt Text](https://github.com/Mohanrajx/Image/blob/54a2b9a61bbfde75dbb29077b050429a2207aca8/code_20240419_125139_via_10015_io.png)


</details>

---
#### 6(C). To write a Python PROGRAM for first come first serve scheduling PROGRAM.
#### PROGRAM
![Alt Text](https://github.com/Mohanrajx/DSD/blob/f8eeeb9c8e97cff48a929784159753e08150db70/code_20240415_184907_via_10015_io.png)

##
<details>
<summary>
Sample Output :
</summary>

![Alt Text](https://github.com/Mohanrajx/Image/blob/48c741f1df267f2f5bda76e294cbba1e9c58bcac/code_20240419_124745_via_10015_io.png)


</details>

---
#### 7(A) To write a Python script for implementing linear search technique.
#### PROGRAM
![Alt Text](https://github.com/Mohanrajx/Image/blob/0e01d3dba820964c4a061007e0321951f53bbd91/code_20240415_225519_via_10015_io.png) 
##

<details>
<summary>
Sample Output :
</summary>

![Alt Text](https://github.com/Mohanrajx/Image/blob/e4c2878593475f7726433751517de63fa6c12df8/code_20240419_120119_via_10015_io.png)


</details>

---

#### 7(B) IMPLEMENTATION OF BINARY SEARCHING TECHNIQUE
###### Write a Python PROGRAM to search an element in a given linear list using recursion 
#### PROGRAM
![Alt Text](https://github.com/Mohanrajx/Image/blob/09c31c02f8d93a60b88cc33d7760279195039b27/code_20240419_121735_via_10015_io.png)
##
<details>
<summary>
Sample Output :
</summary>

![Alt Text](https://github.com/Mohanrajx/Image/blob/e2add4d25153f4ffd8c015d33900eff019d9113a/code_20240419_122033_via_10015_io.png)


</details>

---

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

<details>
<summary>
Sample Output :
</summary>

![Alt Text](https://github.com/Mohanrajx/Image/blob/7f45e8d05288c8113e37d13d29c838b32291a620/code_20240419_122557_via_10015_io.png)


</details>

---

#### 7(D) To write a Python PROGRAM to arrange the given elements using insertion sort.
#### PROGRAM
![Alt Text](https://github.com/Mohanrajx/Image/blob/2ff43a5033a19c67655724387d0b5d84b2db9404/code_20240415_230257_via_10015_io.png)
##
<details>
<summary>
Sample Output :
</summary>

![Alt Text](https://github.com/Mohanrajx/Image/blob/3f131ac64277f6aa860fe72d79455fefb5298dfb/code_20240419_122951_via_10015_io.png)


</details>

---

#### 7(E) To write a Python PROGRAM to arrange the given elements using selection sort.
#### PROGRAM
![Alt Text](https://github.com/Mohanrajx/Image/blob/a15ee04334bcbf4c966f30723dfde5a194cd8aa9/code_20240415_230616_via_10015_io.png)
##
<details>
<summary>
Sample Output :
</summary>

![Alt Text](https://github.com/Mohanrajx/Image/blob/8045453d809d1f05046e3008bc7caa4abfb154dc/code_20240419_123200_via_10015_io.png)


</details>

---

#### 8(A) To write a Python PROGRAM to print a binary tree in vertical order.
#### PROGRAM

![Alt Text](https://github.com/Mohanrajx/DSD/blob/bff99ac3409dd91fbb26ba7bcb630e10d55d75c8/Mohanrajx9A.png)

##
<details>
<summary>
Sample Output :
</summary>

![Alt Text](https://github.com/Mohanrajx/Image/blob/5b0a0634195e3d55c91ad07a9564b14924366ad1/code_20240419_123917_via_10015_io.png)


</details>

---
#### 9A. To write a Python PROGRAM in order to traverse and search element from binary tree 🌲 .
### PROGRAM

<details>
  <summary><h5>74 lines of code</h5></summary>
    
![Alt Text](https://github.com/Mohanrajx/Image/blob/2a59539071a38fd33b14bd288ea21f24ad72f11a/code_20240415_192603_via_10015_io.png)
   
</details>

#### EASIEST VERSION OF CODE
![Alt Text](https://github.com/Mohanrajx/Image/blob/c14efe9ec99c8c01174a9fa3459ea761e1d0f58b/code_20240415_193149_via_10015_io.png)

##
<details>
<summary>
Sample Output :
</summary>

![Alt Text](https://github.com/Mohanrajx/Image/blob/d78a7fa0a3c90ac5eb05e77cb95104aa201bf30f/code_20240419_123509_via_10015_io.png)


</details>

---
### I shall expeditiously conclude the outstanding updates.
##
# GM 



