# Example 1
```python
def perms(s):
    '''
    Permutation - Generate All Possible strings from 1 string
    '''
    if(len(s)==1): return [s]
    result=[]
    for i,v in enumerate(s):
        result += [v+p for p in perms(s[:i]+s[i+1:])]
    return result

print(
    perms('abc adf')
)
```