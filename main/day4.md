# Question 14

### **Question:**

> **_Write a program that accepts a sentence and calculate the number of upper case letters and lower case letters._**

> **_Suppose the following input is supplied to the program:_**

```
Hello world!
```

> **_Then, the output should be:_**

```
UPPER CASE 1
LOWER CASE 9
```

---

**My Solution in Python 3**

```python
try:
	inp = input()
	upper = 0
	lower = 0
	if inp:
		for l in inp:
			if l.isupper():
				upper += 1
			elif l.islower():
				lower += 1

	print(f'UPPER CASE: {upper}\nLOWER CASE: {lower}')
except Exception as err:
	print(f'Error: {err}')
```

---
![day_4_q14](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/73527465-3d45-4a51-8fdd-4821d0066871)

---

# Question 15

### **Question:**

> **_Write a program that computes the value of a+aa+aaa+aaaa with a given digit as the value of a._**

> **_Suppose the following input is supplied to the program:_**

```
9
```

> **_Then, the output should be:_**

```
11106
```
---

**My Solution in Python 3**

```python
def computesItself(num):
	strg = str(num)
	return int(strg) + int(strg*2) + int(strg*3) + int(strg*4)

try:
	digit = int(input())
	print(computesItself(digit))
except Exception as err:
	print(f'Invalid input: {err}')
```

---
![day_4_q15](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/c47d8c64-d343-49d8-a3f7-36e7baf9ebbc)

---
