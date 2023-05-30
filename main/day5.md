# Question 16

### **Question:**

> **_Use a list comprehension to square each odd number in a list. The list is input by a sequence of comma-separated numbers._** >**_Suppose the following input is supplied to the program:_**

```
1,2,3,4,5,6,7,8,9
```

> **_Then, the output should be:_**

```
1,9,25,49,81
```

---

**My Solution in Python 3**

```python
try:
	my_list = [str(int(num)**2) for num in input().split(',') if int(num) % 2 != 0]
	print(','.join(my_list))
except ValueError as err:
	print(f'Invalid input: {err}')
```

---
![day_5_q16](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/5e86e9a9-dc22-46e0-b37b-a6b494fd8063)

---

# Question 17

### **Question:**

> **_Write a program that computes the net amount of a bank account based a transaction log from console input. The transaction log format is shown as following:_**

```
D 100
W 200
```

- D means deposit while W means withdrawal.

> **_Suppose the following input is supplied to the program:_**

```
D 300
D 300
W 200
D 100
```

> **_Then, the output should be:_**

```
500
```

---

**My Solution in Python 3**

```python
def transactionTotal():
	total = 0
	while True:
		try:
			transaction_log = input().split()
			if len(transaction_log) == 1:
				print('Invalid input')
				break
			if not transaction_log:
				break
			if transaction_log[0] == 'D':
				total += int(transaction_log[1])
			elif transaction_log[0] == 'W':
				total -= int(transaction_log[1])
		except Exception as err:
			print(f'Error in input: {err}')
	return total

print('Total is: ',transactionTotal())
```

---
![day_5_q17](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/388218df-d0c3-4a3c-8a6c-57b7be893aaa)

---

