Consider the following code:

```python
class HouseManager:
    MAX_ROOMS = 5  # this is a class-level constant

    def __init__(self):
        self.houses = []


class RoomsError(Exception):  # this is a user-defined exception
    pass


class House:
    def __init__(self, address):
        self.address = address
        self.__rooms = {}  # this is a private variable

    def add_room(self, name, room):
        if len(self.__rooms.keys()) == HouseManager.MAX_ROOMS:
            raise RoomsError()
        self.__rooms[name] = room

    def __room_info(self):
        lines = []
        for name, r in self.__rooms.items():
            lines.append('* ' + name + ' ' + str(r))
        return '\n'.join(lines)

    def __str__(self):
        room_count = len(self.__rooms.keys())
        room_info = self.__room_info()
        return 'The house at ' + self.address + ' has ' + str(room_count) + ' rooms:\n' + room_info + '\n'


class Room:
    def __init__(self, desc):
        self.__desc = desc

    def __str__(self):
        return '[desc: ' + self.__desc + ']'


class LivingRoom(Room):
    def __str__(self):  # overriding a method of the parent class
        return '[type: LivingRoom] ' + super().__str__()


class BedRoom(Room):
    def __str__(self):
        return '[type: BedRoom] ' + super().__str__()


if __name__ == '__main__':
    hm = HouseManager()
    h1 = House('S123456')
    h1.add_room('room1', LivingRoom('main living room'))
    h1.add_room('room2', BedRoom('master bedroom'))
    h1.add_room('room3', BedRoom('guest bedroom'))
    print(h1)
    hm.houses.append(h1)
    hm.houses.append(House('S654321'))
    print(hm.houses[1])
```

When executed, it produces the following output:
```
The house at S123456 has 3 rooms:
* room1 [type: LivingRoom] [desc: main living room]
* room2 [type: BedRoom] [desc: master bedroom]
* room3 [type: BedRoom] [desc: guest bedroom]

The house at S654321 has 0 rooms:
```

(a) Draw a class diagram to represent the classes in the code.

(b) Draw an object diagram to represent the object structure produced by the lines 53-61.