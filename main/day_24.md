# Question 100

### **Question**

> **_You are given words. Some words may repeat. For each word, output its number of occurrences. The output order should correspond with the input order of appearance of the word. See the sample input/output for clarification._**

> **_If the following string is given as input to the program:_**
>
> ```
> 4
> bcdef
> abcdefg
> bcde
> bcdef
> ```
>
> **_Then, the output of the program should be:_**
>
> ```
> 3
> 2 1 1
> ```

---

**My Solution in Python 3**

```python
n = int(input())

word_list = []
word_dict = {}

for i in range(n):
    word = input()
    if word not in word_dict:
        word_list.append(word)
    word_dict[word] = word_dict.get(word, 0) + 1

print(len(word_list))
for word in word_list:
    print(word_dict[word], end=' ')
```

---
![day_24_q100](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/17c6e21c-ba0b-4f77-81f1-35a9356d6c26)

---

# Question 101

### **Question**

> **_You are given a string.Your task is to count the frequency of letters of the string and print the letters in descending order of frequency._**

> **_If the following string is given as input to the program:_**
>
> ```
> aabbbccde
> ```
>
> **_Then, the output of the program should be:_**
>
> ```
> b 3
> a 2
> c 2
> d 1
> e 1
> ```

---

**My Solution in Python 3**

```python
def frequencySort(string):

	freq = {}

	for char in string:
		if char in freq:
			freq[char] += 1
		else:
			freq[char] = 1

	return freq

string = input('Enter a string: ')

result = frequencySort(string)

desc_order = sorted(result.items(),key=lambda x:x[1],reverse=True)

for char in range(len(desc_order)):
	print(desc_order[char][0], desc_order[char][1])

```

---
![day_24_q101](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/3a6b5968-69ef-433a-bf3c-987c39db01ec)

---

# Question 102

### **Question**

> **_Write a Python program that accepts a string and calculate the number of digits and letters._**

**Input**

> ```
> Hello321Bye360
> ```

**Output**

> ```
> Digit - 6
> Letter - 8
> ```

---

**My Solution in Python 3**

```python
def calculateNumbersDigits(string):

	digits = 0
	letters = 0

	for d_or_l in string:
		if 'a' <= d_or_l <= 'z' or 'A' <= d_or_l <= 'Z':
			letters += 1
		elif 0 <= int(d_or_l) <= 9:
			digits += 1

	return digits,letters

string = input('Enter a string: ')

if string:
	digit, letter = calculateNumbersDigits(string)
	print(f'Digit - {digit}\nLetter - {letter}')
```

---
![day_24_q102](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/d0b61d75-3a9a-4881-bd23-5b97e0c1fee3)

---

# Question 103

### **Question**

> **_Given a number N.Find Sum of 1 to N Using Recursion_**

**Input**

> ```
> 5
> ```

**Output**

> ```
> 15
> ```

---


**My Solution in Python 3**

```python
def sumRecursive(number):

	if number < 2:
		return number

	return number + sumRecursive(number-1)

number = int(input('Enter a number: '))

try:
	print(f'Output: {sumRecursive(number)}')
except ValueError as err:
	print(f'Invalid input: {err}')
```

---
![day_24_q103](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/53e82b8e-096e-4f9b-9192-5cf197aa9458)

---
