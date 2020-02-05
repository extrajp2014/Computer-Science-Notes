Recursive Binary Search

```python
def binary_search_recursive(sorted_array, target, low=0, high=None):
    if not sorted_array[0] <= target <= sorted_array[-1]:
        return False
    if high is None:
        high = len(sorted_array) - 1

    mid = (low + high) // 2

    if sorted_array[mid] == target:
        return mid
    elif target < sorted_array[mid]:
        high = mid - 1
    elif sorted_array[mid] < target:
        low = mid + 1

    return binary_search_recursive(sorted_array, target, low, high)
```