# Shape-Calculator

###Scientific Computing with Python, course offered by freecodecamp.org

Practice with Class/Object Inheritance, rectangle and square instances with various methods

Instructions for building this project can be found at https://www.freecodecamp.org/learn/scientific-computing-with-python/scientific-computing-with-python-projects/polygon-area-calculator


      class Rectangle:

          def __init__(self, width, height):
              self.width = width
              self.height = height 

          def __repr__(self):
              return (f"Rectangle(width={self.width}, height={self.height})")

          def set_width(self, width):
              self.width = width

          def set_height(self, height):
              self.height = height

          def get_area(self):
              area = (self.width * self.height)
              return area

          def get_perimeter(self):
              perimeter = 2 * (self.width + self.height)
              return perimeter

          def get_diagonal(self):
              diagonal = ((self.width ** 2 + self.height ** 2) ** .5)
              return diagonal

          def get_picture(self):
              if self.height > 50:
                  return "Too big for picture."
              elif self.width > 50:
                  return "Too big for picture."
              else:
                  picture = (((self.width) * "*") + '\n') * (self.height)
                  return picture

          def get_amount_inside(self, new_shape):   
              amount_inside = self.get_area() // new_shape.get_area()
              return amount_inside

      class Square(Rectangle):

          def __init__(self, side):
              super().__init__(side, side) 

          def __repr__(self):
              return (f"Square(side={self.width}")

          def set_side(self, side):
              self.width = side
              self.height = side
