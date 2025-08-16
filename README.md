# Polygon Area Calculator Project - By: David Kachroo

This public repository contains my solution for the **"Build a Polygon Area Calculator"** project from the **freeCodeCamp Scientific Computing with Python** certification.

## Project Overview
This project uses object-oriented programming to implement two classes, `Rectangle` and `Square`. The `Square` class is a subclass of `Rectangle`, which inherits its methods and attributes while adding specialized functionality.

### Features:
- **Rectangle Class**
  - Initialize with `width` and `height`.
  - `set_width` and `set_height` methods to update dimensions.
  - `get_area`: Returns the area of the rectangle.
  - `get_perimeter`: Returns the perimeter.
  - `get_diagonal`: Returns the diagonal length.
  - `get_picture`: Returns an ASCII representation of the shape (up to 50x50).
  - `get_amount_inside`: Returns how many times another shape can fit inside.
  - String representation: `Rectangle(width=5, height=10)`

- **Square Class**
  - Subclass of `Rectangle`, initialized with a single `side` length.
  - Inherits all `Rectangle` methods.
  - `set_side`: Updates both width and height.
  - Overrides `set_width` and `set_height` to keep the square’s sides equal.
  - String representation: `Square(side=9)`

### Example Usage:
```python
rect = Rectangle(10, 5)
print(rect.get_area())
rect.set_height(3)
print(rect.get_perimeter())
print(rect)
print(rect.get_picture())

sq = Square(9)
print(sq.get_area())
sq.set_side(4)
print(sq.get_diagonal())
print(sq)
print(sq.get_picture())

rect.set_height(8)
rect.set_width(16)
print(rect.get_amount_inside(sq))
