Example 1
```python
class Room:
    def __init__(self, name, description):
        self.name = name
        self.description = description

class Person:
    def __init__(self, current_room):
        self.current_room = current_room

room = {
    'inside':  Room("Living Room",
                     "Where you can relax")
}
personObject = Person(room['inside'])
```

Example 2
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

waypoint = Waypoint(lat=41.70505, lon=-121.51521, name='Catacombs')
```