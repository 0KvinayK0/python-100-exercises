
# Question 51

### **Question**

> ***Write a function to compute 5/0 and use try/except to catch the exceptions.***

---

**My Solution in Python 3**

```python
def computeZeroDivision():
	return 5/0

try:
	print(computeZeroDivision())	
except ZeroDivisionError as err:
	print(f'Error: {err}')
```
---
![day_14_q51](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/11d78bdb-d874-4d8e-b2a0-dbf684882c82)

---


# Question 52

### **Question**

> ***Define a custom exception class which takes a string message as attribute.***

---

**My Solution in Python 3**

```python
class MyException(Exception):
	def __init__(self,mess):
		self.mess = mess

num = input('If I say 10 you say: ')

try:
	if num == '10':
		raise MyException('Not an error! Correct response.')
	else:
		raise MyException('Gibberish!')

except MyException as err:
	print(f'Error: {err}')

```
---
![day_14_q52](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/f7ec3486-39d8-4cf9-ada0-6f75384b9444)

---


# Question 53

### **Question**

> ***Assuming that we have some email addresses in the "username@companyname.com" format, please write program to print the user name of a given email address. Both user names and company names are composed of letters only.***

> ***Example:
If the following email address is given as input to the 
program:***
```
john@google.com
```
> ***Then, the output of the program should be:***
```
john
```
> ***In case of input data being supplied to the question, it should be assumed to be a console input.***

---

**My Solution in Python 3**

```python
def extractUsername(email):

	if not email:
		return None

	username = ''

	for string in email:
		if string == '@':
			break
		else:
			username += string
	return username

try:
	result = extractUsername(input('Enter email: '))
	print(f'Username is: {result}')
except Exception as err:
	print(f'Error: {err}')
```

---
![day_14_q53](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/fd344b5c-ecee-4119-8520-16c54193d742)

---
