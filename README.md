class Human:
    def __init__(self, name):
        self.name = name

class Car:
    def __init__(self, passengers):
        self.passengers = passengers

h1 = Human("Arthur")
h2 = Human("Kate")
h3 = Human("Volodymyr")

# Створення машини з пасажирами
car = Car([h1, h2, h3])

# Виведення імені другого пасажира (індекс 1) з машини
print(car.passengers[1].name)  # Kate
