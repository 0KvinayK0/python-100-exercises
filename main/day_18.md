# Question 70

### **Question**

> **_Please write a program to output a random even number between 0 and 10 inclusive using random module and list comprehension._**

---

**My Solution in Python 3**

```python
from random import randrange

random_number = [randrange(0,10)]
print(random_number)
```

---
![day_18_q70](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/c96a1c62-0f82-4da9-a0f1-cfc9c0f94b5a)


---

# Question 71

### **Question**

> **_Please write a program to output a random number, which is divisible by 5 and 7, between 10 and 150 inclusive using random module and list comprehension._**

---


**My Solution in Python 3**

```python
import random
print random.choice([i for i in range(10,151) if i%5==0 and i%7==0])
```

---

**My Solution: Python 3**

```python
from random import choice

print(choice([i for i in range(10,150) if i % 5 == 0 and i % 7 == 0]))

```

---
![day_18_q71](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/3a9f0807-b0c1-452b-8a2d-2d2fb59de478)

---

# Question 72

### **Question**

> **_Please write a program to generate a list with 5 random numbers between 100 and 200 inclusive._**

---


**My Solution in Python 3**

```python

from random import sample

print(sample(range(100,200),5))
```

---
![day_18_q72](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/984f20e8-4db4-4d7c-b667-dbd96adf862a)


---

# Question 73

### **Question**

> **_Please write a program to randomly generate a list with 5 even numbers between 100 and 200 inclusive._**

---


**My Solution in Python 3**

```python
import random
resp = random.sample(range(100,201,2),5)
print(resp)

```

---


# Question 74

### **Question**

> **_Please write a program to randomly generate a list with 5 numbers, which are divisible by 5 and 7 , between 1 and 1000 inclusive._**

---


**My Solution in Python 3**

```python
from random import sample

print(sample([for i in range(1,1001) if i % 5 == 0 and i % 7 == 0],5))
```

---
![day_18_q74](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/fc1d7baa-8358-4ce4-84f5-40a0d1f5d2af)


---
