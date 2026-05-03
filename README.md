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
class Human:
    def __init__(self, name):
        self.name = name

    def hi(self):
        print("Hi! My name is ", self.name)

class Car:
    def __init__(self, passengers):
        self.passengers = passengers

    def hi_all_passengers(self):
        for p in self.passengers:
            p.hi()

    # Новий метод: додати пасажира
    def add_passenger(self, human):
        self.passengers.append(human)
        print(f"{human.name} доданий до машини!")

h1 = Human("Arthur")
h2 = Human("Kate")
h3 = Human("Volodymyr")

c = Car([h1, h2, h3])

c.hi_all_passengers()

# Використання нового методу
h4 = Human("Sophia")
c.add_passenger(h4)
c.hi_all_passengers()  # Sophia теж привітається
