# Question 26

### **Question:**

> **_Define a function which can compute the sum of two numbers._**

---

**My Solution in Python 3**

```python
def computeSum(num1,num2):
	return num1+num2

try:
	num1 = int(input('Enter the first number: '))
	num2 = int(input('Enter the second number: '))

	print(computeSum(num1,num2))
except ValueError as err:
	print(f'Invalid input: {err}')
```

---
![day_9_q_26](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/bdbc1569-19d6-49e8-bdce-90ea42ee1e40)

---

# Question 27

### **Question:**

> **_Define a function that can convert a integer into a string and print it in console._**

---

**My Solution in Python 3**

```python
def convertIntToString(number):
	return str(number),type(str(number))

try:
	number = int(input())
	print(convertIntToString(number))
except ValueError as err:
	print(f'Invalid input: {err}')
```

---
![day_9_q_27](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/2b7cc13e-b157-4fee-a4f9-f7e999296709)

---

# Question 28

### **Question:**

> **_Define a function that can receive two integer numbers in string form and compute their sum and then print it in console._**

---


**My Solution in Python 3**

```python
def SumStringNum(num1,num2):
	return int(num1)+int(num2)

try:
        num1 = input('Enter the first number: ')
        num2 = input('Enter the second number: ')

        print(SumStringNum(num1,num2))
except ValueError as err:
        print(f'Invalid input: {err}')
```

---
![day_9_q_28](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/2c933958-d874-4771-9420-469d17c04465)

---

# Question 29

### **Question:**

> **_Define a function that can accept two strings as input and concatenate them and then print it in console._**

---


**My Solution in Python 3**

```python
def concatenateTwoStrings(str1,str2):
	return str1 + ' ' + str2

try:
        num1 = input('Enter the string: ')
        num2 = input('Enter the string: ')

        print(concatenateTwoStrings(num1,num2))
except ValueError as err:
        print(f'Invalid input: {err}')
```

---
![day_9_q_29](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/1f79127d-05b8-496c-a97b-ee8ee8cdaeb0)

---

# Question 30

### **Question:**

> **_Define a function that can accept two strings as input and print the string with maximum length in console. If two strings have the same length, then the function should print all strings line by line._**

---

**My Solution in Python 3**

```python
def maximumLengthString(str1,str2):
	if len(str1) == len(str2):
		for char in (str1+str2):
			print(char)
		return 'Done'
	return str1 if len(str1) > len(str2) else str2

try:
        num1 = input('Enter the first string: ')
        num2 = input('Enter the second string: ')

        print(maximumLengthString(num1,num2))
except ValueError as err:
        print(f'Invalid input: {err}')

```

---
![day_9_q_30_1](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/0ce8f69e-f870-4f3c-a0ea-87f1acc2ea9d)
![day_9_q_30_2](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/a1cc140c-712d-4151-a4c1-f66963989157)

---
