class Human:
    def __init__(self, name, energy=100, money=0, knowledge=0):
        self.name = name
        self.energy = energy
        self.money = money
        self.knowledge = knowledge

    def hi(self):
        print("Hi! My name is ", self.name)

    def study(self):
        if self.energy >= 20:
            self.knowledge += 10
            self.energy -= 20

    def work(self):
        if self.energy >= 30:
            self.money += self.knowledge // 5 + 10
            self.energy -= 30

    def rest(self):
        self.energy = min(100, self.energy + 50)

class Car:
    def __init__(self, passengers):
        self.passengers = passengers

    def hi_all_passengers(self):
        for p in self.passengers:
            p.hi()

h1 = Human("Arthur")
h2 = Human("Kate")
h3 = Human("Volodymyr")

c = Car([h1, h2, h3])
c.hi_all_passengers()
