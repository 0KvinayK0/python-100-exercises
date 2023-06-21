# Question 85

### **Question**

> **_By using list comprehension, please write a program to print the list after removing the 0th,4th,5th numbers in [12,24,35,70,88,120,155]._**

---


**My Solution in Python 3**

```python
li = [12,24,35,70,88,120,155]

print([el for i,el in enumerate(li) if i not in (5,4,0)])
```
---
![day_21_q85](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/ce4c8832-137c-4e26-bba4-14ef6408199b)

---

# Question 86

### **Question**

> **_By using list comprehension, please write a program to print the list after removing the value 24 in [12,24,35,24,88,120,155]._**

---

**My Solution in Python 3**

```python
li = [12,24,35,24,88,120,155]
print([i for i in li if i != 24])
```

---

![day_21_q86](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/31e24343-365a-440d-aa66-f07cc8853437)

---

# Question 87

### **Question**

> **_With two given lists [1,3,6,78,35,55] and [12,24,35,24,88,120,155], write a program to make a list whose elements are intersection of the above given lists._**

---


**My Solution in Python 3**

```python
output = []

l2_new = {}
l1 = [1,3,6,78,35,55]
l2 = [12,24,35,24,88,120,155]

for el in l2:
	l2_new[el] = True

for el in l1:
	if el in l2_new:
		output.append(el)

print('Common elements: ',output)
```

---
![day_21_q87](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/816542b7-a66e-4a7b-bbb5-729c97c5c0fc)

---

# Question 88

### **Question**

> **_With a given list [12,24,35,24,88,120,155,88,120,155], write a program to print this list after removing all duplicate values with original order reserved._**

---

**My Solution in Python 3**

```python
numbers = [12,24,35,24,88,120,155,88,120,155]

def removeDuplicates(numbers):
	remove_duplicates = {}

	for num in numbers:
		if num in remove_duplicates:
			continue
		else:
			remove_duplicates[num] = True

	return remove_duplicates.keys()


print(removeDuplicates(numbers))
```

---
![day_21_q88](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/ea42c366-ab65-48f9-bb4f-b408f4730f89)

---


# Question 89

### **Question**

> **_Define a class Person and its two child classes: Male and Female. All classes have a method "getGender" which can print "Male" for Male class and "Female" for Female class._**

---

**My Solution in Python 3**

```python
class Person(object):
	def getGender(self):
		return 'Person'

class Male(Person):
	def getGender(self):
		return 'Male'

class Female(Person):
	def getGender(self):
		return 'Female'


m = Male()
f = Female()
print(f'I am a {m.getGender()}')
print(f'I am a {f.getGender()}')
```

---
![day_21_q89](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/e1c0f7c4-0a77-445e-9785-f5a060d460ee)

---
