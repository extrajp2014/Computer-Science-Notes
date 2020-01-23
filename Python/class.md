Example 1 - Encapsulation
```python
class Room:
    def __init__(self, name, description):
        self.name = name
        self.description = description

class Person:
    def __init__(self, current_room):
        self.current_room = current_room

    def __str__(self):
        # This method is for the user
        store_string = self.current_room
        return store_string

    def __repr__(self):
        # This method is for the developer

    # Encapsulation, data protection for class
    def get_name(self):
        '''
        Getter
        '''
        return self.current_room

    def set_name(self, new_name):
        '''
        Data validation goes here
        Build logic to check new_name meet criteria before reset a data variable

        '''
        self.current_room = new_name

room = {
    'inside':  Room("Living Room",
                     "Where you can relax")
}
personObject = Person(room['inside'])


```

Example 2 - Inheritance
```python
class LatLon:
    
    def __init__(self, lat, lon):
        self.lat = lat
        self.lon = lon

class Waypoint(LatLon):
    
    def __init__(self, lat, lon, name):
        super().__init__(lat, lon)
        self.name = name
        
    def __str__(self):
        return f'"{self.name}", {self.lat}, {self.lon}'

class Geocache(Waypoint):
    def __init__(self, name, difficulty, size, lat, lon):
        self.difficulty = difficulty
        self.size = size
        super().__init__(name, lat, lon)

    def __str__(self):
        return f"{super().__str__()} is inherited from Waypoint class"

waypoint = Waypoint(lat=41.70505, lon=-121.51521, name='Catacombs')
```