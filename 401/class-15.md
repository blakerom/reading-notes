# Trees

Common Terminology

   - Node - A node is the individual item/data that makes up the data structure
   - Root - The root is the first/top Node in the tree
   - Left Child - The node that is positioned to the left of a root or node
   - Right Child - The node that is positioned to the right of a root or node
   - Edge - The edge in a tree is the link between a parent and child node
   - Leaf - A leaf is a node that does not contain any children
   - Height - The height of a tree is determined by the number of edges from the root to the bottommost node

### Traversing
- Pre-order: root>>left>>right
- In-order: left>>root>>right
- Post-order: left>>right>>root

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/tree-example.png)

#### Output
- Pre-order: A, B, D, E, C, F
- In-order: D, B, E, A, F, C
- Post-order: D, E, B, F, C, A

### Algorithms
- Pre-order
```js
ALGORITHM preOrder(root)
// INPUT <-- root node
// OUTPUT <-- pre-order output of tree node's values

    OUTPUT <-- root.value

    if root.left is not Null
        preOrder(root.left)

    if root.right is not NULL
        preOrder(root.right)
```
- In-order
```js
ALGORITHM inOrder(root)
// INPUT <-- root node
// OUTPUT <-- in-order output of tree node's values

    if root.left is not NULL
        inOrder(root.left)

    OUTPUT <-- root.value

    if root.right is not NULL
        inOrder(root.right)
```
- Post-order
```js
ALGORITHM postOrder(root)
// INPUT <-- root node
// OUTPUT <-- post-order output of tree node's values

    if root.left is not NULL
        postOrder(root.left)

    if root.right is not NULL
        postOrder(root.right)

    OUTPUT <-- root.value
```

