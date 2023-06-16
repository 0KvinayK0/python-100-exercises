# Question 75

### **Question**

> **_Please write a program to randomly print a integer number between 7 and 15 inclusive._**

---

**My Solution in Python 3**

```python
from random import randrange

print('Random number between 7 and 15: ',randrange(7,15))
```

---
![day_19_q75](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/54b74a86-e3b8-417c-ada0-ad26b155a593)

---

# Question 76

### **Question**

> **_Please write a program to compress and decompress the string "hello world!hello world!hello world!hello world!"._**

---

**My Solution in Python 3**

```python
import zlib

s = 'hello world!hello world!hello world!hello world!'
y = bytes(s, 'utf-8')
t = zlib.compress(y)
print(f'Original string: {s}')
print(f'Compressed string: {t}')
print('Decompressed string: ',zlib.decompress(t))
```
---
![day_19_q76](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/04b911db-ee93-493c-b86a-47a6bc905abc)

---

# Question 77

### **Question**

> **_Please write a program to print the running time of execution of "1+1" for 100 times._**

---


**My Solution in Python 3**

```python
from time import time

start = time()
for i in range(100):
		print(1+1)
end = time()
total = end - start
print(f'Time taken: {total} seconds')
```

---
![day_19_q77](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/80f910f6-e2c9-4e86-9f16-64ddce778429)

---

# Question 78

### **Question**

> **_Please write a program to shuffle and print the list [3,6,7,8]._**

---

**My Solution in Python 3**

```python

from random import shuffle
li = [3,6,7,8]
shuffle(li)
print li

```

---
![day_19_q78](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/a752b12d-37cc-47e9-a785-eb6bab708fe1)


---

# Question 79

### **Question**

> **_Please write a program to generate all sentences where subject is in ["I", "You"] and verb is in ["Play", "Love"] and the object is in ["Hockey","Football"]._**

---


**My Solution in Python 3**

```python
def generate_sentences(subjects, verbs, objects):
    sentences = []
    for subject in subjects:
        for verb in verbs:
            for obj in objects:
                sentence = f"{subject} {verb} {obj}."
                sentences.append(sentence)
    return sentences

subjects = ["I", "You"]
verbs = ["Play", "Love"]
objects = ["Hockey", "Football"]

sentences = generate_sentences(subjects, verbs, objects)

for sentence in sentences:
    print(sentence)

```

---
![day_19_q79](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/69560b2b-4c70-442d-ad59-b552feeb545e)


---
