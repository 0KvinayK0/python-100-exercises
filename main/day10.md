# Question 31

### **Question:**

> **_Define a function which can print a dictionary where the keys are numbers between 1 and 20 (both included) and the values are square of keys._**

---

**My Solution in Python 3**

```python
num_square = {i:i**2 for i in range(1,21)}
print(num_square)
```

---

![day_10_q31](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/2deee81a-919b-4b63-b59e-5ca8b8efb3d5)

---

# Question 32

### **Question:**

> **_Define a function which can generate a dictionary where the keys are numbers between 1 and 20 (both included) and the values are square of keys. The function should just print the keys only._**

---

**My Solution in Python 3**

```python
def num_square():
	num_square = {}
	for num in range(1,21):
		num_square[num] = num**2
	return num_square.keys()

print(num_square())

```

---
![day_10_q32](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/b170860f-0b82-421b-aa4a-dcfc1099c44e)

---

# Question 33

### **Question:**

> **_Define a function which can generate and print a list where the values are square of numbers between 1 and 20 (both included)._**

---

**My Solution in Python 3**

```python
def squareNumbers():
	printList = []
	for i in range(1,21):
		printList.append(i**2)
	print(printList)

squareNumbers()
```

---

![day_10_q33](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/a2fee6d5-a564-450e-8090-c7453b87a80a)

---

# Question 34

### **Question:**

> **_Define a function which can generate a list where the values are square of numbers between 1 and 20 (both included). Then the function needs to print the first 5 elements in the list._**

---

**My Solution in Python 3**

```python
def firstFiveSquareNum():
	five_num = []
	for num in range(1,21):
		five_num.append(num**2)
	print(five_num[:5])

firstFiveSquareNum()
```

---

![day_10_q34](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/8eb8f6ae-b37a-4e9e-a8a0-b522d1a36b06)

---

# Question 35

### **Question:**

> **_Define a function which can generate a list where the values are square of numbers between 1 and 20 (both included). Then the function needs to print the last 5 elements in the list._**

---

**My Solution in Python 3**

```python
def lastFiveNum():
	last_five = []
	for i in range(1,21):
		last_five.append(i**2)
	return last_five[-5:]

print(lastFiveNum())
```

---
![day_10_q35](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/8d2f58e7-a79b-4a27-8b4d-02a0f0e4e8a5)

---

# Question 36

### **Question:**

> **_Define a function which can generate a list where the values are square of numbers between 1 and 20 (both included). Then the function needs to print all values except the first 5 elements in the list._**

---

**My Solution in Python 3**

```python
def allExceptFive():
        all_not_five = []
        for i in range(1,21):
                all_not_five.append(i**2)
        print(all_not_five[5:])

allExceptFive()
```

---
![day_10_q36](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/c6588c80-0724-46e1-a06c-a86dedbfb974)

---

# Question 37

### **Question:**

> **_Define a function which can generate and print a tuple where the value are square of numbers between 1 and 20 (both included)._**

---


**My Solution in Python 3**

```python
def printTuple():
	num = list()
	for i in range(1,21):
		num.append(i**2)
	print(tuple(num))

printTuple()
```

---
![day_10_q37](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/7575c672-d7b5-47a2-8cb5-ec49c2aebf4e)

---
