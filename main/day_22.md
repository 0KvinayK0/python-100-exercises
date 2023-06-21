# Question 90

### **Question**

> **_Please write a program which count and print the numbers of each character in a string input by console._**

> **_Example:
> If the following string is given as input to the program:_**

```
abcdefgabc
```

> **_Then, the output of the program should be:_**

```
a,2
c,2
b,2
e,1
d,1
g,1
f,1
```

**My Solution in Python 3**

```python
def countString(string):

  count = {}

  for s in string:
    if s in count:
      count[s] += 1
    else:
      count[s] = 1

  return count

string = 'abcdefgabc'
result = countString(string)

print('Input:',string)
print('---Output---')
for key,value in result.items():
  print(key,value)
```

---

![day_22_q90](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/8fdf0d66-ad12-4dc1-9bcd-045ae25c6316)

---

# Question 91

### **Question**

> **_Please write a program which accepts a string from console and print it in reverse order._**

> **Example:
> If the following string is given as input to the program:\***

```
rise to vote sir
```

> **_Then, the output of the program should be:_**

```
ris etov ot esir
```

**My Solution in Python 3**

```python
def reverseString(string):

	buffer = []
	reverse = ''

	for char in string:
		buffer.append(char)

	for _ in range(len(buffer)):
		reverse += buffer.pop()

	return reverse

string = 'soper buhtig rehto ym ta kool a evaH'
print('Original string:',string)
print('Reversed string: ',reverseString(string))
```

---

![day_22_q91](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/093e48c1-2c3d-42d5-968e-26b70743223f)

---

# Question 92

### **Question**

> **_Please write a program which accepts a string from console and print the characters that have even indexes._**

> **_Example:
> If the following string is given as input to the program:_**

```
H1e2l3l4o5w6o7r8l9d
```

> **_Then, the output of the program should be:_**

```
Helloworld
```

**My Solution in Python 3**

```python
def printEvenIndices(string):

	result = ''

	for i in range(len(string)):
		if i % 2 == 0:
			result += string[i]
	return result

string = 'H1e2l3l4o5w6o7r8l9d'
print(f'Original string: {string}')
print(f'Indexed string: {printEvenIndices(string)}')
```

---

![day_22_q92](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/12852654-e254-4c16-8ba7-3874ba68a173)

---

# Question 93

### **Question**

> **_Please write a program which prints all permutations of [1,2,3]_**

---


**My Solution in Python 3**

```python
from itertools import permutations
print(list(permutations([1,0,1])))
```

---
![day_22_q93](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/3b7fee28-4cbe-4b28-bbbf-60f6584f2d17)

---

# Question 94

### **Question**

> **_Write a program to solve a classic ancient Chinese puzzle:
> We count 35 heads and 94 legs among the chickens and rabbits in a farm. How many rabbits and how many chickens do we have?_**

---


**My Solution in Python 3**

```python
def countRabbitChicken(heads,legs):
	
	for chickens in range(heads+1):
		rabbits = heads - chickens
		total_legs = 2 * chickens + 4 * rabbits
		if total_legs == legs:
			return chickens,rabbits
	return None

heads,legs = 35,94

count = countRabbitChicken(heads,legs)
print(f'Chickens: {count[0]}')
print(f'Rabbits: {count[1]}')
```
---
![day_22_q94](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/25d9bd05-ff45-4843-943f-64c4917620fd)


---

