# Question 38

### **Question:**

> **_With a given tuple (1,2,3,4,5,6,7,8,9,10), write a program to print the first half values in one line and the last half values in one line._**

---

**My Solution in Python 3**

```python
tup = (1,2,3,4,5,6,7,8,9,10)
tup1 = list(tup[:5])
tup2 = list(tup[5:])
for num1 in tup1:
	print(num1,end= ' ')
print()
for num1 in tup2:
	print(num1,end= ' ')
```

---

![day_11_q38](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/219fdece-fc47-4c0a-a046-467b192fc91f)

---

# Question 39

### **Question:**

> **_Write a program to generate and print another tuple whose values are even numbers in the given tuple (1,2,3,4,5,6,7,8,9,10)._**

---

**My Solution in Python 3**

```python
tup = (1,2,3,4,5,6,7,8,9,10)

def evenOfTuples(tup):
	tup2 = list()
	for num in tup:
		if num % 2 == 0:
			tup2.append(num)
	return tuple(tup2)

for i in evenOfTuples(tup):
	print(i, end = ' ')
```

---
![day_11_q39](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/83fd810b-9f78-42a8-b020-305659446ba4)

---

# Question 40

### **Question:**

> **_Write a program which accepts a string as input to print "Yes" if the string is "yes" or "YES" or "Yes", otherwise print "No"._**

---


**My Solution in Python 3**

```python
def acceptCaseInsensitiveString(str):
	if str == 'yes' or str == 'YES' or str == 'Yes':
		return 'Yes'
	return 'No'

print(acceptCaseInsensitiveString('YES'))
```

---
![day_11_q40](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/01529592-e2bf-45f5-bf5d-14154235068b)

---

# Question 41

### **Question:**

> **_Write a program which can map() to make a list whose elements are square of elements in [1,2,3,4,5,6,7,8,9,10]._**

---


**My Solution in Python 3**

```python
num = [1,2,3,4,5,6,7,8,9,10]
square_num = list(map(lambda x:x**2,num))
print(square_num)
```

---
![day_11_q41](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/efff2332-c61d-4406-87d5-6a7a108cbacf)

---

# Question 42

### **Question:**

> **_Write a program which can map() and filter() to make a list whose elements are square of even number in [1,2,3,4,5,6,7,8,9,10]._**

---


**My Solution in Python 3**

```python
num = [1,2,3,4,5,6,7,8,9,10]
square_even_num = list(map(lambda x:x**2, filter(lambda x: x%2==0,num)))
print(square_even_num)
```

---
![day_11_q42](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/2bd4032b-e32c-436f-82f5-2e78b648cf2c)

---

# Question 43

### **Question:**

> **_Write a program which can filter() to make a list whose elements are even number between 1 and 20 (both included)._**

---


**My Solution in Python 3**

```python
even_num = list(filter(lambda x: x % 2 == 0, range(1,21)))
print(even_num)
```

---
![day_11_q43](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/18d30d71-dd09-4245-a8dc-4641bdc49c8f)


---
