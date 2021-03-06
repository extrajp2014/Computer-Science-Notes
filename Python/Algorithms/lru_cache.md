```python
class LRUCache:
    """
    Our LRUCache class keeps track of the max number of nodes it
    can hold, the current number of nodes it is holding, a doubly-
    linked list that holds the key-value entries in the correct
    order, as well as a storage dict that provides fast access
    to every node stored in the cache.
    """
    def __init__(self, limit=10):
        self.cache = dict()
        self.limit = limit
        self.storage = DoublyLinkedList()

    """
    Retrieves the value associated with the given key. Also
    needs to move the key-value pair to the end of the order
    such that the pair is considered most-recently used.
    Returns the value associated with the key or None if the
    key-value pair doesn't exist in the cache.
    """
    def get(self, key):
        if key in self.cache:
            self.storage.move_to_front(self.cache[key])
            return self.cache[key].value[key]
        else:
            return None

    """
    Adds the given key-value pair to the cache. The newly-
    added pair should be considered the most-recently used
    entry in the cache. If the cache is already at max capacity
    before this entry is added, then the oldest entry in the
    cache needs to be removed to make room. Additionally, in the
    case that the key already exists in the cache, we simply
    want to overwrite the old value associated with the key with
    the newly-specified value.
    """
    def set(self, key, value):
        if key in self.cache:
            self.cache[key].value[key] = value
            self.storage.move_to_front(self.cache[key])
        else:
            if self.storage.__len__() < self.limit:
                self.storage.add_to_head({key: value})
                self.cache[key] = self.storage.head
            else:
                take_key_out = list(self.storage.remove_from_tail().keys())[0]
                self.cache.pop(take_key_out)
                self.storage.add_to_head({key: value})
                self.cache[key] = self.storage.head

"""Each ListNode holds a reference to its previous node
as well as its next node in the List."""


class ListNode:
    """Each ListNode holds a reference to its previous node
    as well as its next node in the List."""
    def __init__(self, value, prev=None, next=None):
        self.value = value
        self.prev = prev
        self.next = next

    def insert_after(self, value):
        """Wrap the given value in a ListNode and insert it
        after this node. Note that this node could already
        have a next node it is pointing to."""
        current_next = self.next
        self.next = ListNode(value, self, current_next)
        if current_next:
            current_next.prev = self.next

    def insert_before(self, value):
        """Wrap the given value in a ListNode and insert it
        before this node. Note that this node could already
        have a previous node it is pointing to."""
        current_prev = self.prev
        self.prev = ListNode(value, current_prev, self)
        if current_prev:
            current_prev.next = self.prev

    def delete(self):
        """Rearranges this ListNode's previous and next pointers
        accordingly, effectively deleting this ListNode."""
        if self.prev:
            self.prev.next = self.next
        if self.next:
            self.next.prev = self.prev

class DoublyLinkedList:
    """Our doubly-linked list class. It holds references to
    the list's head and tail nodes."""
    def __init__(self, node=None):
        self.head = node
        self.tail = node
        self.length = 1 if node is not None else 0

    def __len__(self):
        return self.length

    """Wraps the given value in a ListNode and inserts it 
    as the new head of the list. Don't forget to handle 
    the old head node's previous pointer accordingly."""
    def add_to_head(self, value):
        if self.head:
            self.head.insert_before(value)
            self.head = self.head.prev
            self.length+=1
        else:
            self.head = ListNode(value)
            self.tail = self.head
            self.length+=1

    """Removes the List's current head node, making the
    current head's next node the new head of the List.
    Returns the value of the removed Node."""
    def remove_from_head(self):
        if not self.head:
            return None
        self.length -= 1

        # improve logic
        if self.head is self.tail:
            current_head = self.head
            self.head = None
            self.tail = None
            return current_head.value
        else:
            current_head = self.head
            self.head = self.head.next
            self.head.prev = None
            return current_head.value

    """Wraps the given value in a ListNode and inserts it 
    as the new tail of the list. Don't forget to handle 
    the old tail node's next pointer accordingly."""
    def add_to_tail(self, value):
        self.length += 1
        new_node = ListNode(value, None, None)

        if self.head:
            self.tail.next = new_node
            new_node.prev = self.tail
            self.tail = new_node
        # elif not self.head and not self.tail:
        else:
            self.head = new_node
            self.tail = new_node

    """Removes the List's current tail node, making the 
    current tail's previous node the new tail of the List.
    Returns the value of the removed Node."""
    def remove_from_tail(self):
        self.length -= 1
        if not self.tail:
            return None
        elif self.head is self.tail:
            current_tail = self.tail
            self.head = None
            self.tail = None
            return current_tail.value
        else:
            current_tail = self.tail
            self.tail = self.tail.prev
            self.tail.next = None
            return current_tail.value

    """Removes the input node from its current spot in the 
    List and inserts it as the new head node of the List."""
    def move_to_front(self, node):
        if node is self.head:
            return None
        elif node is self.tail:
            self.remove_from_tail()
        else:
            self.delete(node)
            self.length -= 1
        self.add_to_head(node.value)

    """Removes the input node from its current spot in the 
    List and inserts it as the new tail node of the List."""
    def move_to_end(self, node):
        if node is self.tail:
            return None
        elif node is self.head:
            self.remove_from_head()
        else:
            self.delete(node)
            self.length -= 1
        self.add_to_tail(node.value)

    """Removes a node from the list and handles cases where
    the node was the head or the tail"""
    def delete(self, node):
        if node is self.head:
            self.remove_from_head()
        if node is self.tail:
            self.remove_from_tail()

    """Returns the highest value currently in the list"""
    def get_max(self):
        if not self.head:
            return None

        max_value = self.head.value
        current = self.head
        while current:
            if current.value > max_value:
                max_value = current.value
            current = current.next

        return max_value
```