Selection Sort
```python
def selection_sort( arr ):
    # loop through n-1 elements
    for i in range(len(arr) - 1):
        cur_index = i
        smallest_index = cur_index
        # find next smallest element
        for j in range(cur_index, len(arr)):
            if arr[j] < arr[smallest_index]:
                smallest_index = j

        # swap
        arr[cur_index], arr[smallest_index] = arr[smallest_index], arr[cur_index]

    return arr
```