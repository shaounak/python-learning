---
marp: true
theme: default
paginate: true
---

# Polymorphism in Python
## Shaounak Nasikkar
### 07/15/2024

---

## Introduction

### What is Polymorphism?

  * Ability of objects to respond differently to the same method call
  * Core concept in object-oriented programming (OOP)
  * Enables flexible and reusable code

### Benefits of Polymorphism

  * Cleaner code structure
  * Reduced code duplication
  * Improved maintainability

---

## Inheritance: Foundation of Polymorphism

* Inheritance allows classes to inherit properties and methods from parent classes
* Subclasses (children) can specialize behavior of inherited methods

---

## Example - Shape Class Hierarchy

```python
class Shape:
  def area(self):
    raise NotImplementedError("Subclasses must implement area()")

class Rectangle(Shape):
  def __init__(self, width, height):
    self.width = width
    self.height = height

  def area(self):
    return self.width * self.height

class Circle(Shape):
  def __init__(self, radius):
    self.radius = radius

  def area(self):
    return 3.14 * self.radius**2
```

---

* `Shape` is a base class with an abstract `area` method
* `Rectangle` and `Circle` inherit from `Shape` and implement `area`

---

## Polymorphic Behavior

```python
def calculate_total_area(shapes):
  total_area = 0
  for shape in shapes:
    total_area += shape.area()  # Polymorphic call - uses object's specific area()
  return total_area

shapes = [Rectangle(5, 3), Circle(2)]
total_area = calculate_total_area(shapes)
print(f"Total Area: {total_area}")
```

* `calculate_total_area` works with any object with an `area` method
* Polymorphism allows for generic code that adapts to different object types

---

## Duck Typing

* Principle: If it walks like a duck and quacks like a duck, then it must be a duck
* Focuses on object behavior rather than specific class type
* Python relies heavily on duck typing for polymorphism

---

## Example - Duck Typing with a Speakable Interface**

```python
class Animal:
  def make_sound(self):
    raise NotImplementedError("Subclasses must implement make_sound()")

class Dog(Animal):
  def make_sound(self):
    print("Woof!")

class Cat(Animal):
  def make_sound(self):
    print("Meow!")

# Function using duck typing
def make_animal_speak(animal):
  animal.make_sound()  # Duck typing - assumes object has a make_sound() method

dog = Dog()
cat = Cat()

make_animal_speak(dog)
make_animal_speak(cat)
```

---

* `Animal` is an abstract class with a `make_sound` method
* `Dog` and `Cat` implement `make_sound` with their specific sounds
* `make_animal_speak` works with any object with a `make_sound` method

---

## Conclusion

* Polymorphism is a powerful concept in Python
* Enables flexible, reusable, and maintainable code
* Achieved through inheritance and duck typing strategies