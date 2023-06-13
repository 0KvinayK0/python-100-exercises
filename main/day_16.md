# Question 60

### **Question**

> **_Write a program to compute:_**

```
f(n)=f(n-1)+100 when n>0
and f(0)=0
```

> **_with a given n input by console (n>0)._**

> **_Example:
> If the following n is given as input to the program:_**

```
5
```

> **_Then, the output of the program should be:_**

```
500
```

> **_In case of input data being supplied to the question, it should be assumed to be a console input._**

---


**My Solution in Python 3**

```python
def computeRecursion(n):
	if n == 0:
		return n
	return computeRecursion(n-1) + 100

try:
	n = int(input('Enter a number greater than zero: '))
	if n < 0:
		print(f'Enter number greater than 0!: {n}')
	else:
		print('Output: ',computeRecursion(n))
except Exception as err:
	print(f'Invalid input: {err}')
```

---
![day_16_q60](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/c4c4e395-3735-4685-a892-ce4951258f99)

---

# Question 61

### **Question**

> **_The Fibonacci Sequence is computed based on the following formula:_**

```
f(n)=0 if n=0
f(n)=1 if n=1
f(n)=f(n-1)+f(n-2) if n>1
```

> **_Please write a program to compute the value of f(n) with a given n input by console._**

> **_Example:
> If the following n is given as input to the program:_**

```
7
```

> **_Then, the output of the program should be:_**

```
13
```

> **_In case of input data being supplied to the question, it should be assumed to be a console input._**

---

**My Solution in Python 3**

```python
def fibonacci(n):
	if n < 2:
		return n
	return fibonacci(n-1) + fibonacci(n-2)

try:
	n = int(input('Enter index: '))
	if n > 0:
		print('Output: ',fibonacci(n))
except Exception as err:
	print(f'Invalid input: {err}')
```

---
![day_16_q61](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/14ac5317-afc1-497b-8893-ed6154903d0c)

---

# Question 62

### **Question**

> **_The Fibonacci Sequence is computed based on the following formula:_**

```
f(n)=0 if n=0
f(n)=1 if n=1
f(n)=f(n-1)+f(n-2) if n>1
```

> **_Please write a program to compute the value of f(n) with a given n input by console._**

> **_Example:
> If the following n is given as input to the program:_**

```
7
```

> **_Then, the output of the program should be:_**

```
0,1,1,2,3,5,8,13
```

> **_In case of input data being supplied to the question, it should be assumed to be a console input._**

---


**My Solution in Python 3**

```python
def fibonacci(n):
	fib = [0,1]
	for i in range(2,n+1):
		fib.append(fib[i-1]+fib[i-2])

	return fib

try:
        n = int(input('Enter index: '))
        if n > 0:
                print('Output: ',fibonacci(n))
except Exception as err:
        print(f'Invalid input: {err}')

```

---
![day_16_q62](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/d8dc066c-b247-4d6e-9467-83010bd975da)

---

# Question 63

### **Question**

> **_Please write a program using generator to print the even numbers between 0 and n in comma separated form while n is input by console._**

> **_Example:
> If the following n is given as input to the program:_**

```
10
```

> **_Then, the output of the program should be:_**

```
0,2,4,6,8,10
```

> **_In case of input data being supplied to the question, it should be assumed to be a console input._**

---


**My Solution in Python 3**

```python
def generatorEven(n):
	for num in range(n):
		if num % 2 == 0:
			yield num


try:
	n = int(input())
	for i in generatorEven(n+1):
		print(i,end=',')
except Exception as err:
        print(f'Invalid input: {err}')

```

---

![day_16_q63](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/32bcf9dd-3981-4c27-bfc8-3363cee932ee)

---

# Question 64

### **Question**

> **_Please write a program using generator to print the numbers which can be divisible by 5 and 7 between 0 and n in comma separated form while n is input by console._**

> **_Example:
> If the following n is given as input to the program:_**

```
100
```

> **_Then, the output of the program should be:_**

```
0,35,70
```

> **_In case of input data being supplied to the question, it should be assumed to be a console input._**

---


**My Solution in Python 3**

```python
def generatorDiv(n):
	for num in range(n):
		if num % 5 == 0 and num % 7 == 0:
			yield num

try:
        n = int(input())
        print(','.join([str(i) for i in generatorDiv(n+1)]))             
except Exception as err:
        print(f'Invalid input: {err}')
```

---
![day_16_q64](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/8b88076e-d8da-48c0-aef2-a40d05f701fc)

---
