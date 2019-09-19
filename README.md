# data_structures_pre-order_traversal
Data Structures Pre-Order Traversal

1. Check if the current node is empty/null
2. Dipslay the data part of the root (or current node)
3. Traverse the left subtree by recursively calling the pre-order function
4. Traverse the right treaveby recursively calling the pre-order function


```
class Node(object):
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right = None
        
class BinaryTree(object):
    def __init__(self, root):
        
    def print_tree(self, traversal_type): # helper function
    
        
    def preorder_print(self, start, traversal):  # start will be updated on every recursive call. traversal is str for print
        """Root->Left->Right"""
        if start:
            traversal += (str(start.value) + "-") # print value and append to traversal string
            traversal = self.preorder_print(start.left, traversal) # call func, go down left side
            traversal = self.preorder_print(start.right, traversal) # same as above, but to the right
        return traversal
    

```
