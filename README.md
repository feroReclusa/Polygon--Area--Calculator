# Polygon--Area--Calculator
import math

class Polygon:
    def __init__(self, sides, length):
        self.sides = sides
        self.length = length

    def perimeter(self):
        return self.sides * self.length

    def area(self):
        apothem = self.length / (2 * math.tan(math.pi / self.sides))
        return 0.5 * self.perimeter() * apothem

    def __str__(self):
        return f"A {self.sides}-sided polygon with length {self.length}"

# Example usage
triangle = Polygon(3, 5)
print(triangle)
print("Perimeter:", triangle.perimeter())
print("Area:", triangle.area())

hexagon = Polygon(6, 7)
print(hexagon)
print("Perimeter:", hexagon.perimeter())
print("Area:", hexagon.area())
