# Question 44

### **Question:**

> **_Write a program which can map() to make a list whose elements are square of numbers between 1 and 20 (both included)._**

---

**My Solution in Python 3**

```python
print(list(map(lambda x:x**2,range(1,21))))
```

---
![day_12_q44](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/632386bc-311d-4527-af34-817aad14d490)

---

# Question 45

### **Question:**

> **_Define a class named American which has a static method called printNationality._**

---


**My Solution in Python 3**

```python
class American():
	
	@staticmethod
	def printNationality():
		print('American!!')

American.printNationality()
```

---
![day_12_q45](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/2281881b-4706-45c4-a658-dad4af34bdc6)

---

# Question 46

### **Question:**

> **_Define a class named American and its subclass NewYorker._**

---


**My Solution in Python 3**

```python
class American():
	def __init__(self):
		self.name = 'Clark'

	def shoutName(self):
		return f'My name is {self.name}'

class NewYorker(American):
	def __init__(self):
		super().__init__()

	def shoutParentName(self):
		return f'I live in New York, and my name is {self.name}'

ny = NewYorker()
print(ny.shoutParentName())
```

---

![day_12_q46](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/63a46df0-5a0b-44be-a09f-6c144f5b63fa)

---
