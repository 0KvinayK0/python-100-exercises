# Question 20

### **Question:**

> **_Define a class with a generator which can iterate the numbers, which are divisible by 7, between a given range 0 and n._**

> **_Suppose the following input is supplied to the program:_**

```
7
```

> **_Then, the output should be:_**

```
0
7
14
```
---

**My Solution in Python 3**

```python
class DivisibleBySeven():
  def generator(self,num):
    for i in range(num+1):
      if i % 7 == 0:
        yield i

d1 = DivisibleBySeven()
for j in d1.generator(13):
  print(j)
```

---
![day_7_q20](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/4fa717a3-6067-4e2c-b0e4-ac35dc642319)
---

# Question 21

### **Question:**

> **_A robot moves in a plane starting from the original point (0,0). The robot can move toward UP, DOWN, LEFT and RIGHT with a given steps. The trace of robot movement is shown as the following:_**

```
UP 5
DOWN 3
LEFT 3
RIGHT 2
```

> **_The numbers after the direction are steps. Please write a program to compute the distance from current position after a sequence of movement and original point. If the distance is a float, then just print the nearest integer._**
> **_Example:_**
> **_If the following tuples are given as input to the program:_**

```
UP 5
DOWN 3
LEFT 3
RIGHT 2
```

> **_Then, the output of the program should be:_**

```
2
```

---

**My Solution in Python 3**

```python
from math import sqrt

def calculateDistance():
	y_axis = 0
	x_axis = 0

	while True:
		direction = input().split()
		if not direction:
			break
		if direction[0] == 'UP':
			y_axis += int(direction[1])
		elif direction[0] == 'DOWN':
			y_axis -= int(direction[1])
		elif direction[0] == 'LEFT':
			x_axis += int(direction[1])
		elif direction[0] == 'RIGHT':
			x_axis -= int(direction[1])
		else:
			break
	return round(sqrt(x_axis**2+y_axis**2))

print(calculateDistance())
```

---
![day_7_q21](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/09210bb8-3a60-413f-a7cf-b068a639a824)

---
