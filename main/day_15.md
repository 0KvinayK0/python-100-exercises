# Question 54

### **Question**

> **_Assuming that we have some email addresses in the "username@companyname.com" format, please write program to print the company name of a given email address. Both user names and company names are composed of letters only._**

> **_Example:
> If the following email address is given as input to the program:_**

```
john@google.com
```

> **_Then, the output of the program should be:_**

```
google
```

> **_In case of input data being supplied to the question, it should be assumed to be a console input._**

---


**My Solution in Python 3**

```python
def extractCompanyName(email):
  index = 0
  for ind,char in enumerate(email):
    if char == '@':
      index += ind + 1
      
  if index == 0:
    return f'Invalid email: {email}'
    
  company_name = email[index:]

  return company_name

try:
  email = input('Enter an email: ')
  print(extractCompanyName(email))
except Exception as err:
  print(f'Invalid input: {err}')
```

---
![day_15_q54](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/70dac626-bcd6-4406-bed5-10ce9d635a8c)

---

# Question 55

### **Question**

> **_Write a program which accepts a sequence of words separated by whitespace as input to print the words composed of digits only._**

> **_Example:
> If the following words is given as input to the program:_**

```
2 cats and 3 dogs.
```

> **_Then, the output of the program should be:_**

```
['2', '3']
```

> **_In case of input data being supplied to the question, it should be assumed to be a console input._**

---


**My Solution in Python 3**

```python
def isDigit(sentence):

	digit = []
	for word in sentence:
		if word.isnumeric():
			digit.append(word)

	if not digit:
		return None
	return digit

try:
	sentence = input('Enter a sentence: ').split()
	print(isDigit(sentence))
except Exception as err:
	print(f'Invalid input: {err}')
```

---
![day_15_q55](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/5949014c-72df-42ef-a8e0-0b31ebbad89a)

---

# Question 56

### **Question**

> **_Print a unicode string "hello world"._**

---


**My Solution in Python 3**

```python
unicode_string = u'This is a unicode string'
print(unicode_string)
```

---
![day_15_q56](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/d5c19961-8622-487f-9eb5-f76c37cdb2f2)
---


# Question 57

### **Question**

> **_Write a program to read an ASCII string and to convert it to a unicode string encoded by utf-8._**

---

**My Solution in Python 3**

```python
s = input()
u = s.encode('utf-8')
print(f'This is a unicode string: {u}')
```

---

![day_15_q57](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/ed7499a1-d39c-4f82-b1c8-24b4566b5d1f)

---

# Question 58

### **Question**

> **_Write a special comment to indicate a Python source code file is in unicode._**

---


**My Solution in Python 3**

```python
# -*- coding: utf-8 -*-
```

---

# Question 59

### **Question**

> **_Write a program to compute 1/2+2/3+3/4+...+n/n+1 with a given n input by console (n>0)._**

> **_Example:
> If the following n is given as input to the program:_**

```
5
```

> **_Then, the output of the program should be:_**

```
3.55
```

> **_In case of input data being supplied to the question, it should be assumed to be a console input._**

---

**My Solution in Python 3**

```python
def computeOperation(n):
    return round(sum(map(lambda x: x/(x+1), range(1, n+1))), 2)

try:
	n = int(input())
	print('Output: ',computeOperation(n))
except Exception as err:
	print(f'Invalid input: {err}')
```

---
![day_15_q59](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/a633fa7d-b398-4fa8-8715-0616217ec00d)

---
