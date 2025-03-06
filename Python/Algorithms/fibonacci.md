# Fibonacci using recursion

```python
def fib(n):
    '''
    fib with recursion, runtime O(2^n)
    '''
    if n < 2:
        return 1
    else:
        return fib(n-1) + fib(n-2)

def fib_cache(n, cache=dict()):
    '''
    fib with recursion & caching, runtime O(n)
    '''
    if cache and cache[n] != 0:
        return cache[n]
    else:
        if not cache:
            cache = [0]*n
            cache[0] = 1
            cache[1] = 1
            cache[n] = fib_cache(n-1, cache) + fib_cache(n-2, cache)
        return cache[n]

if __name__ == '__main__':
    fib(6)
    fib_cache(6)
```