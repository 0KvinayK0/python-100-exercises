# Question 22

### **Question:**

> **_Write a program to compute the frequency of the words from the input. The output should output after sorting the key alphanumerically._**

> **_Suppose the following input is supplied to the program:_**

```
New to Python or choosing between Python 2 and Python 3? Read Python 2 or Python 3.
```

> **_Then, the output should be:_**

```
2:2
3.:1
3?:1
New:1
Python:5
Read:1
and:1
between:1
choosing:1
or:2
to:1
```

---

**My Solution in Python 3**

```python
from pprint import pprint
try:
	words = input().split()
	pprint({word:words.count(word) for word in words})
except Exception as err:
	print(f'Invalid input: {err}')
```

---
![day_8_q22](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/a147d2ea-01ee-4ceb-8e36-438ab72da7fd)

---

# Question 23

### **Question:**

> **_Write a method which can calculate square value of number_**

---

**My Solution in Python 3**

```python
def squareNumber(num):
	return int(num)**2
try:
	numbers = input().split(',')
	print('\n'.join([str(num)for num in (list(map(squareNumber,numbers)))]))
except ValueError as err:
	print(f'Invalid Input: {err}')
  ```

---
![day_8_q23](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/bab4a457-04bb-4d08-ab32-334a5feb03bd)

---

# Question 24

### **Question:**

> **_Python has many built-in functions, and if you do not know how to use it, you can read document online or find some books. But Python has a built-in document function for every built-in functions._**

> **_Please write a program to print some Python built-in functions documents, such as abs(), int(), raw_input()_**

> **_And add document for your own function_**

---

**My Solution in Python 3**

```python
from math import sqrt

class ChangingDunder():
	def __init__(self,value):
		self.value = value

	def abs(self):
		'''
		This returns the absolute/positive value for the input number
		'''
		return int(sqrt(self.value**2))

try:
	cd = ChangingDunder(int(input()))
	print(cd.abs())
except ValueError as err:
	print(f'Invalid input: {err}')
```

---
![day_8_q24](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/68bb8071-4ac2-46fa-93a0-61d030a51c70)

---

# Question 25

### **Question:**

> **_Define a class, which have a class parameter and have a same instance parameter._**

---

**My Solution in Python 3**

```python
class Magical():
	def __init__(self,name,power,speciality):
		self.name = name
		self.power = power	
		self.speciality	= speciality	

	def shoutName(self):
		return f'Ahhhhhh, it is {self.name}'

	def powerLevel(self):
		return f'Power level of {self.power}'

	def specialAttack(self):
		return f'Attacking with speciality \'{self.speciality}\''

m1 = Magical('Robin',100,'Backflip Ice Thrower')

print(m1.shoutName(),'with a',m1.powerLevel(),',',m1.specialAttack())
```

---
![day_8_q25](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/1f1acbea-9ad4-49a8-895e-eb461be581ab)

---
