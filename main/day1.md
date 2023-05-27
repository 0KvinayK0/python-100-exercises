# Question 1

### **Question:**

> **_Write a program which will find all such numbers which are divisible by 7 but are not a multiple of 5,
> between 2000 and 3200 (both included).The numbers obtained should be printed in a comma-separated sequence on a single line._**

---

**My Solution in Python 3**

```python
li = []
for num in range(2000,3201):
	if num % 7 == 0 and num % 5 != 0:
		li.append(str(num))

print(','.join(li))

```
---
![day_1_q1](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/7deb3ae0-b8db-40a6-ac24-0f81baf3e546)

---

# Question 2

### **Question:**

> **_Write a program which can compute the factorial of a given numbers.The results should be printed in a comma-separated sequence on a single line.Suppose the following input is supplied to the program: 8
> Then, the output should be:40320_**

---

**My Solution in Python 3**

```python
def rec(num):
	if num == 0:
		return 1
	else:
		return num*rec(num-1)

try:
	fact = input().split(',')
	# print(fact)
	for num in fact:
		print(f'Factorial of {num} is : {rec(int(num))}')
except Exception as err:
	print(f'Please try again: {err}')

```
---
![day_1_q2](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/2b2284f8-e668-4b8b-aa23-b8f2a0133c2e)

---

# Question 3

### **Question:**

> **_With a given integral number n, write a program to generate a dictionary that contains (i, i x i) such that is an integral number between 1 and n (both included). and then the program should print the dictionary.Suppose the following input is supplied to the program: 8_**

> **_Then, the output should be:_**


```
{1: 1, 2: 4, 3: 9, 4: 16, 5: 25, 6: 36, 7: 49, 8: 64}
```

---

**My Solution in Python 3**

```python
def intergral_gen(n):
 my_dict = {k:k*k for k in range(1,n+1)}
 return my_dict

try:
    int_num = input().split(',')
    for ind in int_num:
        print(intergral_gen(int(ind)))
except Exception as err:
    print(f'Error running: {err}')
finally:
    print('All done!')

```

---

![day_1_q3](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/0da5de70-6a42-4755-9a38-8ba604e9ad02)

---

