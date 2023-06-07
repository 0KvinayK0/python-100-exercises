# Question 47

### **Question**

> **_Define a class named Circle which can be constructed by a radius. The Circle class has a method which can compute the area._**

---

**My Solution in Python 3**

```python
class Circle():
	def __init__(self,radius):
		self.radius = radius
		self.PI = 3.14

	def area(self):
		return (self.PI * (self.radius**2))

try:
	c = Circle(int(input('Enter the radius: ')))
	print('Area:',c.area())
except ValueError as err:
	print(f'Invalid radius: {err}')
```

---
![day_13_q47](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/19dee455-017f-4034-8f74-7249abbf13bb)

---

# Question 48

### **Question**

> **_Define a class named Rectangle which can be constructed by a length and width. The Rectangle class has a method which can compute the area._**

---


**My Solution in Python 3**

```python
class Rectangle():
	def __init__(self,l,w):
		self.length = l
		self.width = w

	def area(self):
		return self.length*self.width

try:
	length = int(input('Enter length: '))
	width = int(input('Enter width: '))

	r = Rectangle(abs(length),abs(width))
	print('Area of rectangle: ',r.area())
except ValueError as err:
	print(f'Invalid input: {err}')

```

---

![day_13_q48](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/cbe64cc9-7dd5-49df-9217-f2de0dba3981)

---

# Question 49

### **Question**

> **_Define a class named Shape and its subclass Square. The Square class has an init function which takes a length as argument. Both classes have a area function which can print the area of the shape where Shape's area is 0 by default._**

---

**My Solution in Python 3**

```python
class Shape():
    def area(self):
        return 0

class Square(Shape):
    def __init__(self, length):
        super().__init__()
        self.length = length

    def area(self):
        return self.length ** 2

sq = Square(5)
print(sq.area())  # Output: 25
print(super(Square, sq).area())  # Output: 0
```

---
![day_13_q49](https://github.com/0KvinayK0/python-100-exercises/assets/126001522/5751a1e1-628d-4a5a-96b3-e7fd8d8e5c4a)


---

# Question 50

### **Question**

> **_Please raise a RuntimeError exception._**

---


**My Solution in Python 3**

```python
raise RuntimeError('Run!')
```

---
