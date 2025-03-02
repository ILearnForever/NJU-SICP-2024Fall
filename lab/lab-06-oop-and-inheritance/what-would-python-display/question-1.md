# Question 1

> Use Ok to test your knowledge with the following "What Would Python Display?" questions:
>
> ```shell
> python ok -q q1 -u
> ```
>
> **Important**: Type `Function` if you believe the answer is `<function...>`, `Error` if it errors, and `Nothing` if nothing is displayed.

Below is the definition of a `Car` class that we will be using in the following WWPD questions.

```python
class Car(object):
    num_wheels = 4
    gas = 30
    headlights = 2
    size = 'Tiny'
    def __init__(self, make, model):
        self.make = make
        self.model = model
        self.color = 'No color yet. You need to paint me.'
        self.wheels = Car.num_wheels
        self.gas = Car.gas
    def paint(self, color):
        self.color = color
        return self.make + ' ' + self.model + ' is now ' + color
    def drive(self):
        if self.wheels < Car.num_wheels or self.gas <= 0:
            return 'Cannot drive!'
        self.gas -= 10
        return self.make + ' ' + self.model + ' goes vroom!'
    def pop_tire(self):
        if self.wheels > 0:
            self.wheels -= 1
    def fill_gas(self):
        self.gas += 20
        return 'Gas level: ' + str(self.gas)
```

```python
>>> deneros_car = Car('Tesla', 'Model S')
>>> deneros_car.model

______
>>> deneros_car.gas = 10
>>> deneros_car.drive()

______
>>> deneros_car.drive()

______
>>> deneros_car.fill_gas()

______
>>> deneros_car.gas

______
>>> Car.gas

______
>>> deneros_car = Car('Tesla', 'Model S')
>>> deneros_car.wheels = 2
>>> deneros_car.wheels

______
>>> Car.num_wheels

______
>>> deneros_car.drive()

______
>>> Car.drive()

______
>>> Car.drive(deneros_car)

______
```

For the following, we reference the `MonsterTruck` class below.

```python
class MonsterTruck(Car):
    size = 'Monster'
    def rev(self):
        print('Vroom! This Monster Truck is huge!')
    def drive(self):
        self.rev()
        return Car.drive(self)
```

```python
>>> deneros_car = MonsterTruck('Monster', 'Batmobile')
>>> deneros_car.drive()

______
>>> Car.drive(deneros_car)

______
>>> MonsterTruck.drive(deneros_car)

______
>>> Car.rev(deneros_car)

______
```
