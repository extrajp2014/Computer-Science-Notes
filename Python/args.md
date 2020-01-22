#*args - Example
```python
def f2(*args):
    return sum([*args])

a = [7, 6, 5, 4]
print(f2(7, 9, 1, 3, 4, 9, 0))  # Should print 33
print(f2(*a))    # Should print 22

def f3(x, *args):
    if len([*args]) == 0:
        return x + 1
    else: 
        return x + sum([*args])

print(f3(1, 2))  # Should print 3
print(f3(8))     # Should print 9
```

# *kwargs - Example
```python
def f4(**kwargs):  
    for key, value in kwargs.items(): 
        print ("%s: %s" %(key, value))

f4(city="Berkeley", population=121240, founded="March 23, 1868")

d = {
    "monster": "goblin",
    "hp": 3
}
f4(**d)
```