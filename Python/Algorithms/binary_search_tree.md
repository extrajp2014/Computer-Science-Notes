Binary Search Tree Example:

```python
class BinarySearchTree:
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right = None

    # Insert the given value into the tree
    def insert(self, value):
        if value > self.value:
            if not self.right:
                self.right =BinarySearchTree(value)
            else:
                self.right.insert(value)
        else:
            if not self.left:
                self.left = BinarySearchTree(value)
            else:
                self.left.insert(value)


    # Return True if the tree contains the value
    # False if it does not
    def contains(self, target):
        if self.value == target:
            return True
        elif (self.value < target) and self.right:
            return self.right.contains(target)
        elif (target < self.value) and self.left:
            return self.left.contains(target)
        else:
            return False

    # Return the maximum value found in the tree
    def get_max(self):
        # METHOD 1 - ITERATIVE
        current = self
        while current.right:
            current=current.right
        return current.value

        #  METHOD 2 - RECURSIVE
        # Base Case
        if self.right is None:
            return self.value
        # Recursive Case
        else:
            return self.right.get_max()

    # Call the function `cb` on the value of each node
    # You may use a recursive or iterative approach
    def for_each(self, cb):
        # calling function on current node
        cb(self.value)

        # recursive case:
        if self.left:
            self.left.for_each(cb)
        if self.right:
            self.right.for_each(cb)

    # Alternative iternative for_each - example only and not being used
    def iter_for_each(self, cb):
        if self is None:
            print("BST is empty")
            return
        cb(self.value)
        while len(stack) > 0:
            # pop top of stack
            # cb (top of stack)
            # go left ... if left child, push onto stack
            # go right ... if right child, push onto stack
            pass
```