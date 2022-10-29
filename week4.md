## Multiway Tries(MWTs)
### Trie
- Elements are denoted by the **concatenation** of the labels on the path from the root to the node.
### Methods
- Find
   - Starting at root, find a path for each letter in the word.
   - The end node have to be labeled as **"world node."**
- Remove
   - If find failed, do nothing.
   - Else, remove word label from the end node.
- Insert
   - follow find alorithm until cannot find next node.
   - create new nodes until finish insert letter.
- O(k) run time
## Ternary Search Tree
### Structure
- Nodes are arranged similar to Binary Search Tree
- Each Node has three children: Left, Right, Mid
- right child must smaller than middle child, left child must be larger than mid child.
- mid child stand for next character 
### Mehods
- Find
   - If letter is less than node's label: If node has a left child, traverse down to node's left child. Otherwise, we have failed (key does not exist in this Ternary Search Tree)
   - If letter is greater than node's label: If node has a right child, traverse down to node's right child. Otherwise, we have failed (key does not exist in this Ternary Search Tree)
   - If letter is equal to node's label: If letter is the last letter of key and if node is labeled as a "word node," we have successfully found key in our Ternary Search Tree; if not, we have failed. Otherwise, if node has a middle child, traverse down to node's middle child and set letter to the next character of key; if not, we have failed (key does not exist in this Ternary Search Tree)