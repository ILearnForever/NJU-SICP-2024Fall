# Problem 3: Trees (600pts)

Recall that the `tree` abstract data types mentioned in class, can be recursively defined using a root node and (sub)trees.

Tree ADT has one **constructor**:

* `tree(label, branches=[])`: Creates a tree with the given label and branches.

We also have the following default selectors in order to get the information for each tree:

* `label(tree)`: returns the `tree`'s label.
* `branches(tree)`: returns the `tree`'s branches.
* `is_leaf(object)`: returns the if a `tree` is a leaf.
