# The extended part of the repository starts from this page. Previous 94 problems were collected from the repository mentioned in intro. The following problems are collected from Hackerrank and other resources from internet.All the given solutions are in python 3.

# Question 95

### **Question**

> **_Given the participants' score sheet for your University Sports Day, you are required to find the runner-up score. You are given scores. Store them in a list and find the score of the runner-up._**

> **_If the following string is given as input to the program:_**
>
> ```
> 5
> 2 3 6 6 5
> ```
>
> **_Then, the output of the program should be:_**
>
> ```
> 5
> ```

---

**My Solution in Python 3**

```python
def findRunnerUp(n,scores):
	if n < 2:
		return 'Insufficient scores'

	max_score = scores[0]
	runner_up = scores[1]

	for m in range(1,n):
		if scores[m] > max_score:
			max_score = scores[m]
			
	for i in range(2,n):
		if scores[i] < max_score and scores[i] > runner_up:
			runner_up = scores[i]
		
	return runner_up

n = int(input('Number of scores: '))
user_input = input().split(' ')
scores = [int(num) for num in user_input]
print('Runner up: ',findRunnerUp(n, scores))
```

---
![day_23_q95](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/1a89a2aa-4da8-46d2-8c1d-1a7a02e728b0)

---

# Question 96

### **Question**

> **_You are given a string S and width W.
> Your task is to wrap the string into a paragraph of width._**

> **_If the following string is given as input to the program:_**
>
> ```
> ABCDEFGHIJKLIMNOQRSTUVWXYZ
> 4
> ```
>
> **_Then, the output of the program should be:_**
>
> ```
> ABCD
> EFGH
> IJKL
> IMNO
> QRST
> UVWX
> YZ
> ```

---

**My Solution in Python 3**

```python
def stringOfParagraph(string,width):

	counter = -1

	for wrap in string:
		counter += 1
		if counter % width == 0:
			print('\n')
		print(wrap,end='')

string = input()
width = int(input())


if string and width and len(string) >= width:
	stringOfParagraph(string,width)

```

---
![day_23_q96](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/46a5dea7-2977-4d28-8251-3617982f4610)

---


# Question 97

### **Question**

> **_You are given an integer, N. Your task is to print an alphabet rangoli of size N. (Rangoli is a form of Indian folk art based on creation of patterns.)_**

> **_Different sizes of alphabet rangoli are shown below:_**
>
> ```
> #size 3
>
> ----c----
> --c-b-c--
> c-b-a-b-c
> --c-b-c--
> ----c----
>
> #size 5
>
> --------e--------
> ------e-d-e------
> ----e-d-c-d-e----
> --e-d-c-b-c-d-e--
> e-d-c-b-a-b-c-d-e
> --e-d-c-b-c-d-e--
> ----e-d-c-d-e----
> ------e-d-e------
> --------e--------
> ```

---

**My Solution in Python 3**

```python
import string
def print_rangoli(size):
    n = size
    alph = string.ascii_lowercase
    width = 4 * n - 3

    ans = []
    for i in range(n):
        left = '-'.join(alph[n - i - 1:n])
        mid = left[-1:0:-1] + left
        final = mid.center(width, '-')
        ans.append(final)

    if len(ans) > 1:
        for i in ans[n - 2::-1]:
            ans.append(i)
    ans = '\n'.join(ans)
    print(ans)


if __name__ == '__main__':
    n = int(input())
    print_rangoli(n)
```
---
![day_23_q97](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/da931d5e-b4df-466c-a6fa-a9d416ff44cf)

---

# Question 98

### **Question**

> **_You are given a date. Your task is to find what the day is on that date._**

**Input**

> **_A single line of input containing the space separated month, day and year, respectively, in MM DD YYYY format._**
>
> ```
> 08 05 2015
> ```

**Output**

> **_Output the correct day in capital letters._**
>
> ```
> WEDNESDAY
> ```

---


**My Solution in Python 3**

```python
import calendar

month, day, year = map(int, input().split())

dayId = calendar.weekday(year, month, day)
print(calendar.day_name[dayId].upper())
```

---
![day_23_q98](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/e5a33a07-5790-450a-a59c-08bf0877b400)

---

# Question 99

### **Question**

> **_Given 2 sets of integers, M and N, print their symmetric difference in ascending order. The term symmetric difference indicates those values that exist in either M or N but do not exist in both._**

**Input**

> **_The first line of input contains an integer, M.The second line contains M space-separated integers.The third line contains an integer, N.The fourth line contains N space-separated integers._**
>
> ```
> 4
> 2 4 5 9
> 4
> 2 4 11 12
> ```

**Output**

> **_Output the symmetric difference integers in ascending order, one per line._**
>
> ```
> 5
> 9
> 11
> 12
> ```

---

**My Solution in Python 3**

```python
if __name__ == '__main__':
    n = int(input())
    set1 = set(map(int,input().split()))

    m = int(input())
    set2 = set(map(int, input().split()))

    ans = list(set1 ^ set2)
    ans.sort()
    for i in ans:
        print(i)
```

---
![day_23_q99](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/d42a8cbd-755a-4d04-80e8-94ae7f9e3273)

---
