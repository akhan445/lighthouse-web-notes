# Data Structures

Data structes allow us to store and organize groups of data so they can be managed more efficiently.
- Most common ones in js are arrays and objects

## **Arrays**

Great for lists especially when **order matters**

## **Objects**

Allow us to look up data **quickly**

## **Trees**

Hierarchical data structure

Relational

Recursive data structure

![tree-structure](https://miro.medium.com/max/975/1*PWJiwTxRdQy8A_Y0hAv5Eg.png)

***NODE*** - represents a key entity and contains data about that entity
- i.e entity = employee, data = name

***EDGE*** - connection between nodes

***ROOT*** - has no parent

***LEAF*** - has no children

Every node other than root or leaf node has **1 parent and 1 or more children**
- node with same parent --> siblings

### **Sub Trees**

Since trees are recursive data structures, then trees are just made up of sub trees which themselves are made up of even smaller sub trees.

Every node other than root is a **root of a smaller tree** within that tree structure

### **Tree Traversal**

Usually, only a reference to the **root node** is kept instead of a reference to every node

Traversing a tree is similar to iteration over an object or array

#### *Breadth First Traversal*

Visit the nodes closest to root first (all children) then those further away. **row by row**

Root --> Root's child --> Siblings (if any) --> First node's child (grandchild) --> siblings of grandchild --> ...


![bft-traversal](https://i.imgur.com/eW8w8as.png)

#### *Depth First Traversal*

Visit all nodes on a path before visiting nodes on next path.

DFT is a **recursive traversal**
  1. visit root node
  2. get the first unvisited child sub tree of current node
  3. do step 1 with sub tree
  
Root --> Root child --> 1st node child --> 2nd node child --> ... --> leaf --> Then move on to next (parent's next sibling)

![dft-traversal](https://i.imgur.com/C7eQxFV.png)

Like walking **around the tree**

![dft-example](https://i.imgur.com/mY1NJKJ.png)