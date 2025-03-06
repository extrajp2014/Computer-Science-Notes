# Quick Sort

```python
def quick_sort(arr):
    """
    O(nlogn) average run time
    """
    if len(arr) <= 1:
        return arr
    else:
        pivot = arr[len(arr) // 2]
        left = [x for x in arr if x < pivot]
        mid = [x for x in arr if x == pivot]
        right = [x for x in arr if x > pivot]

    return quick_sort(left) + mid + quick_sort(right)
```

```python
def quicksort(arr):
    '''
    O(nlogn) average run time
    '''
    if len(arr) < 2:
        return arr
    else:
        left, right = [], []
        pivot = arr[0]
        for item in arr[1:]:
            if pivot < item:
                left.append(pivot)
            else:
                right.append(pivot)

    return quicksort(left) + [pivot] + quicksort(right)
```