# Question 18

### **Question:**

> **_A website requires the users to input username and password to register. Write a program to check the validity of password input by users._**

> **_Following are the criteria for checking the password:_**

- **_At least 1 letter between [a-z]_**
- **_At least 1 number between [0-9]_**
- **_At least 1 letter between [A-Z]_**
- **_At least 1 character from [$#@]_**
- **_Minimum length of transaction password: 6_**
- **_Maximum length of transaction password: 12_**

> **_Your program should accept a sequence of comma separated passwords and will check them according to the above criteria. Passwords that match the criteria are to be printed, each separated by a comma._**

> **_Example_**

> **_If the following passwords are given as input to the program:_**

```
ABd1234@1,a F1#,2w3E*,2We3345
```

> **_Then, the output of the program should be:_**

```
ABd1234@1
```

---

**My Solution in Python 3**

```python
import re

try:
	a = input('Enter passwords: ').split(',')
	pass_pattern = re.compile(r"^(?=.*[0-9])(?=.*[a-z])(?=.*[A-Z])(?=.*[$#@]).{6,12}$")
	valid_pass = []
	for i in a:
	    if pass_pattern.fullmatch(i):
	        valid_pass.append(i)
	print(','.join(valid_pass))
except Exception as err:
	print(f'Error occured: {err}')
```

---
![day_6_q18](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/ace2270b-1dc5-436a-9e71-e87228e94acd)

---

# Question 19

### **Question:**

> **_You are required to write a program to sort the (name, age, score) tuples by ascending order where name is string, age and score are numbers. The tuples are input by console. The sort criteria is:_**

- **_1: Sort based on name_**
- **_2: Then sort based on age_**
- **_3: Then sort by score_**

> **_The priority is that name > age > score._**

> **_If the following tuples are given as input to the program:_**

```
Tom,19,80
John,20,90
Jony,17,91
Jony,17,93
Json,21,85
```

> **_Then, the output of the program should be:_**

```
[('John', '20', '90'), ('Jony', '17', '91'), ('Jony', '17', '93'), ('Json', '21', '85'), ('Tom', '19', '80')]
```

---

**My Solution in Python 3**

```python
def sortedChars():
    info = []
    try:
        while True:
            chars = tuple(input().split(','))
            if len(chars) < 3:
                break
            
            info.append(chars)
        info.sort(key=lambda x:(x[0],int(x[1]),int(x[2])))
        return info
    except Exception as err:
        print(f'Error: {err}')

print(sortedChars())
```

---
![day_6_q19](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/fd849f98-8642-45b0-91d4-9c67242801cd)

---
