# Question 65

### **Question**

> **_Please write assert statements to verify that every number in the list [2,4,6,8] is even._**

---

**My Solution in Python 3**

```python
data = [2,4,5,6]
for i in data:
    assert i%2 == 0, f"{i} is not an even number"
```

---
![day_17_q65](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/28ca6da0-1ed9-41a3-a840-4d716411dd02)

---

# Question 66

### **Question**

> **_Please write a program which accepts basic mathematic expression from console and print the evaluation result._**

> **_Example:
> If the following n is given as input to the program:_**

```
35 + 3
```

> **_Then, the output of the program should be:_**

```
38
```

---


**My Solution in Python 3**

```python
try:
	n = input('Enter a mathematical expression(Eg. 35 * 4): ')
	print(eval(n))
except Exception as err:
	print(f'Invalid input: {err}')
```

---
![day_17_q66](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/f181eb61-5d4e-47d7-ab49-53fef99f3e19)


---

# Question 67

### **Question**

> **_Please write a binary search function which searches an item in a sorted list. The function should return the index of element to be searched in the list._**

---

**My Solution in Python 3**

```python
def binary_search(lst, target):
    low = 0
    high = len(lst) - 1
    
    while low <= high:
        mid = round((low + high) / 2)
        
        if lst[mid] == target:
            return True
        elif lst[mid] > target:
            high = mid - 1
        else:
            low = mid + 1
    return None
  
 
lst = [1,3,5,7,9]
print(f'From array: {lst}, target is 9, and the result is: ',binary_search(lst, 9)) 

```

---
![day_17_q67](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/252c11c5-78e2-4793-bb4d-722812357bfd)

---

# Question 68

### **Question**

> **_Please generate a random float where the value is between 10 and 100 using Python module._**

---


**My Solution in Python 3**

```python
from random import randrange

print(float(randrange(10,100)))
```

---
![day_17_q68](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/187e032d-c251-4db4-b6e6-20213b60be14)

---

# Question 69

### **Question**

> **_Please generate a random float where the value is between 5 and 95 using Python module._**

---

**My Solution in Python 3**

```python
from random import randrange

print(float(randrange(5,95)))
```

---
![day_17_q69](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/0da2a8cc-3496-400d-b999-3989fcf3c1c5)



---
