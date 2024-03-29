# data_structures_pre-order_traversal
Data Structures Pre-Order Traversal

1. Check if the current node is empty/null
2. Display the data part of the root (or current node)
3. Traverse the left subtree by recursively calling the pre-order function
4. Traverse the right subtree by recursively calling the pre-order function

```
             1
           /   \
          2     3
         / \   / \
        4   5 6   7
```

```
class Node(object):
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right = None
        
class BinaryTree(object):
    def __init__(self, root):
        selt.root = Node(root)
        
    def print_tree(self, traversal_type): # helper function
        if traversal_type == "preorder":
            return self.preorder_print(tree.root, "") # start root & emptry string stores results
        elif traversal_type == "inorder":
            return self.inorder print(tree.root, "")
        else:
            print("Traversal type " + str(traversal_type) + " is not supported.")
            return False
        
    def preorder_print(self, start, traversal):  # start will be updated on every recursive call. traversal is str for print
        """Root->Left->Right"""
        if start:
            traversal += (str(start.value) + "-") # print value and append to traversal string
            traversal = self.preorder_print(start.left, traversal) # call func, go down left side
            traversal = self.preorder_print(start.right, traversal) # same as above, but to the right
        return traversal
        
        
    def inorder_print(self, start, traversal):
    """Left->Root->Right"""
        if start:
            traversal = self.inorder_print(start.left, traversal)
            traversal += (str(start.value) + "-")
            traversal = self.inorder_print(start.right, traversal)
        return traversal
        
        
tree = BinaryTree(1)
tree.root.left = Node(2)
tree.root.right = Node(3)
tree.root.left.left = Node(4)
tree.root.left.right = Node(5)
tree.root.right.left = Node(6)
tree.root.right.right = Node(7)
    
tree.print_tree("preorder")
```
