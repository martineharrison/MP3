MP3: Classes
============

Part 1: `Rectangle`
-------------------

Define a class `Rectangle` which stores the bottom-left coordinates (`x0`, `y0`)
and top-right coordinates (`x1`, `y1`) for each instance. The class should have
the following methods:

    def __init__(self, x0: float, y0: float, x1: float, x2: float):
        ...

    def area(self) -> float:
        """Returns the area of the rectangle."""
        ...

    def contains(self, x: float, y: float) -> bool:
        """Returns true iff the point (x, y) falls within the rectangle"""
        ...

### What to turn in

-   A class definition `Rectangle` defined as above
-   A few basic `assert` tests of the `area` and `contains` methods
-   A brief (paragraph or so) description of your approach and any challenges
    you ran into

### Hints

-   Look up the formula for the area of a rectangle, if you need to
-   Remember that you can't write `a < x < b` in Python; instead, you have to
    write `a < x and x < b`

### Stretch goal

Modify the class so that instead of storing the bottom-left and top-right
coordinates, you simply store the bottom-left coordinates, the height, and the
width, of the rectangle.

Part 2: `Employee` and file reader
----------------------------------

Define a class `Employee` which stores an employee's name, title, and employee
ID, as follows.

    def __init__(self, name: str, title: str, employee_id: int):
        ...

Then, define a function or generator which reads `Employee` data from a text
file and yields fully-populated `Employee` instances.

    from typing import Iterator


    def read_employees(path: str) -> Iterator[Employee]:
        ...

This function should assume the data is formatted similarly to the attached
[`employees.txt`](employees.txt).

### What to turn in

-   A class definition `Employees` defined as above
-   A function or generator `read_employees` defined as above
-   A few basic `assert` tests of `read_employees`
-   A brief (paragraph or so) description of your approach and any challenges
    you ran into

### Hints

-   Use the `with` construction in `read_employees`
-   An example of reading four lines at a time appears in [Lecture
    8](https://nbviewer.jupyter.org/gist/kylebgorman/1053d41c3b44df2571217381ca902889)
