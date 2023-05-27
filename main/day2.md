# Question 4

### **Question:**

> **_Write a program which accepts a sequence of comma-separated numbers from console and generate a list and a tuple which contains every number.Suppose the following input is supplied to the program:_**

```
34,67,55,33,12,98
```

> **_Then, the output should be:_**

```
['34', '67', '55', '33', '12', '98']
('34', '67', '55', '33', '12', '98')
```
---
**My Solution in Python 3**

```python
try:
	nums = list(input('Enter numbers comma-separated: ').split(','))
	t = tuple(nums)
	print(nums)
	print(t)
except Exception as err:
	print(f'Invalid input: {err}')
```
---
![day_2_q1](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/ebfc41c2-499e-44d4-9499-51ffbe0f3695)

---


# Question 5

### **Question:**

> **_Define a class which has at least two methods:_**
>
> - **_getString: to get a string from console input_**
> - **_printString: to print the string in upper case._**

> **_Also please include simple test function to test the class methods._**

---

**My Solution in Python 3**

```python
class Strings():
	def __init__(self):
		self.s = ''

	def getString(self):
		self.s = input()

	def printString(self):
		return self.s.upper()


strs = Strings()
strs.getString()
print(strs.printString())
```
---
![day_2_q2](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/8780da47-11d4-4bac-b07b-c04af09f40b0)

---


# Question 6

### **Question:**

> **_Write a program that calculates and prints the value according to the given formula:_**

> **_Q = Square root of [(2 _ C _ D)/H]_**

> **_Following are the fixed values of C and H:_**

> **_C is 50. H is 30._**

> **_D is the variable whose values should be input to your program in a comma-separated sequence.For example
> Let us assume the following comma separated input sequence is given to the program:_**

```
100,150,180
```

> **_The output of the program should be:_**

```
18,22,24
```

---

**My Solution in Python 3**

```python
from math import sqrt

try:
	d = input('Enter comma-separated num: ').split(',')
	output = []
	for i in d:
		output.append(str(round(sqrt(2*50*int(i)/30))))
	print(','.join(output))
except Exception as err:
	print(f'Invalid input: {err}')
```
---
![day_2_q3](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/d874aa0b-5b7b-48d1-b9f0-47adfe59c7b6)

---

# Question 7

### **Question:**

> **_Write a program which takes 2 digits, X,Y as input and generates a 2-dimensional array. The element value in the i-th row and j-th column of the array should be i _ j.\***

> **_Note: i=0,1.., X-1; j=0,1,¡­Y-1. Suppose the following inputs are given to the program: 3,5_**

> **_Then, the output of the program should be:_**

```
[[0, 0, 0, 0, 0], [0, 1, 2, 3, 4], [0, 2, 4, 6, 8]]
```

---

**My Solution in Python 3**

```python
try:
    x,y = map(int,input().split(','))
    lst = []

    for i in range(x): 
        tmp = []
        for j in range(y): 
            tmp.append(i*j) 
        lst.append(tmp) 

    print(lst)
except Exception as err:
    print(f'Error: {err}')
```
---
![day_2_q7](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/891dd3e2-04de-429a-8214-19bd6b7847e8)

---

# Question 8

### **Question:**

> **_Write a program that accepts a comma separated sequence of words as input and prints the words in a comma-separated sequence after sorting them alphabetically._**

> **_Suppose the following input is supplied to the program:_**

```
without,hello,bag,world
```

> **_Then, the output should be:_**

```
bag,hello,without,world
```

---

**My Solution in Python 3**

```python
try:
	li = input().split(',')
	print(','.join(sorted(li)))
except Exception as err:
	print('Invalid input: {err}')
```
---
![day_2_q8](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/0b56aff4-3d74-436b-b035-f19304fec1c8)

---

# Question 9

### **Question:**

> **_Write a program that accepts sequence of lines as input and prints the lines after making all characters in the sentence capitalized._**

> **_Suppose the following input is supplied to the program:_**

```
Hello world
Practice makes perfect
```

> **_Then, the output should be:_**

```
HELLO WORLD
PRACTICE MAKES PERFECT
```

---

**My Solution in Python 3**

```python
sentence = []

while True:
    try:
        line = input('Enter sentences on new line each: ')
        if not type(line) == 'str':
            break
        if not line:
            break
        else:
            sentence.append(line.upper())
    except Exception as err:
        print(f'Error: {err}')

if sentence:
    for s in sentence:
    	print(s)
```

---
![day_2_q9](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/d21e6d62-5939-47b5-8064-772fc5430048)

---
