# Binary Search Tree (BST) Algorithm

## Methods

### `constructor(array)`
- Initializes the tree by building a balanced binary search tree from the given array.

### `#prepareArray(array)`
- Prepares the input array by removing duplicates and sorting it.

### `buildTree(array, start = 0, end = array.length - 1)`
- Recursively builds a balanced binary search tree from a sorted array.

### `insert(value, node = this.root)`
- Inserts a value into the tree while maintaining the binary search tree structure.
- Rebalances the tree if necessary.

### `delete(value, node = this.root)`
- Deletes a value from the tree and maintains the binary search tree structure.
- Rebalances the tree if necessary.

### `#minValue(node)`
- Finds the minimum value node in a given subtree.

### `find(value, node = this.root)`
- Searches for a node with a specific value.

### `levelOrder(cb, root = this.root)`
- Performs a level-order (BFS) traversal of the tree.
- Optionally executes a callback function on each node.

### `preOrder(cb, node = this.root)`
- Performs a pre-order (DFS) traversal of the tree.
- Optionally executes a callback function on each node.

### `postOrder(cb, node = this.root)`
- Performs a post-order (DFS) traversal of the tree.
- Optionally executes a callback function on each node.

### `inOrder(cb, node = this.root)`
- Performs an in-order (DFS) traversal of the tree.
- Optionally executes a callback function on each node.

### `height(node)`
- Returns the height of a subtree starting from the given node.

### `depth(node, current = this.root, depth = 0)`
- Returns the depth of a specific node within the tree.

### `isBalanced()`
- Checks whether the tree is balanced by comparing the heights of the left and right subtrees.

### `rebalance()`
- Rebalances the tree by reconstructing it from a level-order traversal of the nodes.

### `prettyPrint(node = this.root, prefix = "", isLeft = true)`
- Pretty prints the tree structure to the console, visually representing the hierarchy of nodes.

## Usage

```javascript
const tree = new Tree([10, 20, 5, 15, 30, 25, 35]);

// Insert a new value
tree.insert(40);

// Delete a value
tree.delete(15);

// Find a node
const node = tree.find(20);

// Traversals
tree.levelOrder((node) => console.log(node.value));
tree.preOrder((node) => console.log(node.value));

// Pretty print the tree structure
tree.prettyPrint();
