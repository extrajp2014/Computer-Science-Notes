# Example
```python
import subprocess
try:
    py2output = subprocess.check_output(['python', 'py2.py', '-i', 'test.txt'],stderr= subprocess.STDOUT)  
    #print('py2 said:', py2output)
    print "here"
except subprocess.CalledProcessError as e:
    print "Calledprocerr"

try:
    subprocess.check_output(...)
except subprocess.CalledProcessError as e:
    print e.output
```

