# Question 10

### **Question**

> **_Write a program that accepts a sequence of whitespace separated words as input and prints the words after removing all duplicate words and sorting them alphanumerically._**

> **_Suppose the following input is supplied to the program:_**

```
hello world and practice makes perfect and hello world again
```

> **_Then, the output should be:_**

```
again and hello makes perfect practice world
```
---

**My Solution in Python 3**

```python
sen = sorted(set([word for word in input().split() if isinstance(word,str)]))
print(' '.join(sen))
```

---
![day_3_q10](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/fc7e392a-7d48-4fa8-a34a-3f87636657ed)

---

# Question 11

### **Question**

> **_Write a program which accepts a sequence of comma separated 4 digit binary numbers as its input and then check whether they are divisible by 5 or not. The numbers that are divisible by 5 are to be printed in a comma separated sequence._**

> **_Example:_**

```
0100,0011,1010,1001
```

> **_Then the output should be:_**

```
1010
```

> **_Notes: Assume the data is input by console._**

---

**My Solution in Python 3**

```python
try:
	decimal = input().split(',')
	result = [deci for deci in decimal if int(deci,2) % 5 ==0]
	print(','.join(result))
except Exception as err:
	print(f'Invaid input: {err}')
```
---
![day_3_q11](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/15197951-c303-4521-bf8b-c3111e709f95)

---


# Question 12

### **Question:**

> **_Write a program, which will find all such numbers between 1000 and 3000 (both included) such that each digit of the number is an even number.The numbers obtained should be printed in a comma-separated sequence on a single line._**

---

**My Solution in Python 3**

```python
print(','.join([str(num) for num in range(1000, 3001) if all(map(lambda num: int(num) % 2 == 0, str(num)))]))
```

---
![day_3_q12](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/abd214ba-418c-4ed1-950f-a42bb38eca4f)

---

# Question 13

### **Question:**

> **_Write a program that accepts a sentence and calculate the number of letters and digits._**

> **_Suppose the following input is supplied to the program:_**

```
hello world! 123
```

> **_Then, the output should be:_**

```
LETTERS 10
DIGITS 3
```

---

**My Solution in Python 3**

```python
try:
	word = input()
	letter, digit = 0,0

	for i in word:
		if i.isalpha():
			letter += 1
		elif i.isnumeric():
			digit += 1

	print(f'Letters: {letter}, digits: {digit}')
except Exception as err:
	print(f'Error: {err}')
```

---
![day_3_q13](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/1f707d09-5ab2-4dc1-8a4a-9daa1b1feeb2)

---

