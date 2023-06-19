# Question 80

### **Question**

> **_Please write a program to print the list after removing even numbers in [5,6,77,45,22,12,24]._**

---

**My Solution in Python 3**

```python
print('Even numbers are: ', ','.join([str(i) for i in filter(lambda x: x % 2 == 0,[5,6,77,45,22,12,24])]))
```

---
![day_20_q80](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/3f04be05-18c5-4884-a2e4-ab9bcb3d4366)


---

# Question 81

### **Question**

> **_By using list comprehension, please write a program to print the list after removing numbers which are divisible by 5 and 7 in [12,24,35,70,88,120,155]._**

---

**My Solution in Python 3**

```python
print('List that is divisible by 5 and 7: ',list(filter(lambda x: x%5==0 and x%7== 0,[12,24,35,70,88,120,155])))
```

---
![day_20_q81](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/0247e1a5-dc1e-462b-84d9-e207e16c1062)


---

# Question 82

### **Question**

> **_By using list comprehension, please write a program to print the list after removing the 0th, 2nd, 4th,6th numbers in [12,24,35,70,88,120,155]._**

---


**My Solution in Python 3**

```python
def trimList(arr):

	arr.pop(6)
	arr.pop(4)
	arr.pop(2)
	arr.pop(0)
	return arr

arr = [12,24,35,70,88,120,155]

print('Remaining numbers: ',trimList(arr))
```

---
![day_20_q82](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/377e1ae9-bf63-43d1-8b7f-5af5db08132d)

---

# Question 83

### **Question**

> **_By using list comprehension, please write a program to print the list after removing the 2nd - 4th numbers in [12,24,35,70,88,120,155]._**

---

**My Solution in Python 3**

```python
arr = [12,24,35,70,88,120,155]

print([arr[i] for i in range(len(arr)) if i < 3 or i > 4])

```
---
![day_20_q83](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/611813f3-8b02-4d2a-87ac-dced03a86f0d)

---

# Question 84

### **Question**

> **_By using list comprehension, please write a program generate a 3\*5\*8 3D array whose each element is 0._**

---

**My Solution in Python 3**

```python
array = [[ [0 for col in range(8)] for col in range(5)] for row in range(3)]
print(array)
```

---
![day_20_q84](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/73aeaffe-e62b-4dc4-b805-29ab88a6f0dc)

---
