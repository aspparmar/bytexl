<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif;
      line-height: 1.6;
      color: #2c3e50;
      max-width: 900px;
      margin: 0 auto;
      padding: 20px;
      background-color: #ffffff;
    }
    .lesson-meta {
      color: #7f8c8d;
      font-size: 14px;
      margin-bottom: 8px;
      border-bottom: 2px solid #3498db;
      padding-bottom: 10px;
    }
    h1 {
      color: #2c3e50;
      font-size: 32px;
      margin: 10px 0 20px 0;
    }
    h2 {
      color: #2c3e50;
      font-size: 22px;
      margin-top: 30px;
      margin-bottom: 15px;
      border-left: 4px solid #3498db;
      padding-left: 15px;
    }
    .intro-box {
      background-color: #ecf0f1;
      padding: 20px;
      border-radius: 6px;
      margin: 20px 0;
      border-left: 4px solid #3498db;
    }
    .definition-box {
      background-color: #e8f4f8;
      padding: 15px 20px;
      border-radius: 6px;
      margin: 15px 0;
      border-left: 4px solid #3498db;
    }
    .key-point {
      background-color: #fff9e6;
      padding: 15px 20px;
      border-radius: 6px;
      margin: 15px 0;
      border-left: 4px solid #f39c12;
    }
    .property-box {
      background-color: #f0f8f0;
      padding: 15px 20px;
      border-radius: 6px;
      margin: 15px 0;
      border-left: 4px solid #27ae60;
    }
    .warning-box {
      background-color: #ffe6e6;
      padding: 15px 20px;
      border-radius: 6px;
      margin: 15px 0;
      border-left: 4px solid #e74c3c;
    }
    .image-placeholder {
      background: #f0f0f0;
      border: 2px dashed #ccc;
      padding: 40px;
      text-align: center;
      margin: 20px 0;
      border-radius: 6px;
      color: #666;
    }
    .pseudocode {
      background: #2c3e50;
      color: #ecf0f1;
      padding: 15px 20px;
      border-radius: 6px;
      margin: 15px 0;
      font-family: 'Courier New', monospace;
      font-size: 14px;
      line-height: 1.8;
    }
    .pseudocode-title {
      color: #3498db;
      font-weight: bold;
      margin-bottom: 10px;
    }
    ul, ol {
      margin: 15px 0;
      padding-left: 30px;
    }
    li {
      margin: 8px 0;
    }
    table {
      width: 100%;
      border-collapse: collapse;
      margin: 20px 0;
    }
    th, td {
      border: 1px solid #dee2e6;
      padding: 12px;
      text-align: left;
    }
    th {
      background-color: #3498db;
      color: white;
    }
    tr:nth-child(even) {
      background-color: #f8f9fa;
    }
  </style>
</head>
<body>

<div class="lesson-meta">
  Unit 1.1: Binary Trees and Binary Search Trees | Lesson 2 of 4
</div>

<h1>Binary Search Trees (BST)</h1>

<div class="intro-box">
  <p><strong>Binary Search Trees (BST)</strong> are binary trees with a special ordering property: for every node, all values in the left subtree are smaller, and all values in the right subtree are larger. This property enables efficient searching, insertion, and deletion operations in O(log n) time for balanced trees.</p>
  
  <p>BSTs power countless applications: databases use them for indexing, compilers maintain symbol tables with them, and operating systems rely on them for resource management. Understanding BSTs is fundamental to mastering advanced data structures like AVL trees, Red-Black trees, and B-trees.</p>
</div>

<h2>The BST Property</h2>

<div class="definition-box">
  <p><strong>BST Invariant:</strong> For every node N with value V:</p>
  <ul>
    <li>All values in the left subtree of N are <strong>less than</strong> V</li>
    <li>All values in the right subtree of N are <strong>greater than</strong> V</li>
    <li>Both left and right subtrees are also Binary Search Trees</li>
  </ul>
  <p>This recursive property must hold for every node in the tree, not just the root.</p>
</div>

<div class="image-placeholder">
  <strong>IMAGE: Valid vs Invalid BST</strong><br>
  Left side: Valid BST with nodes following ordering property<br>
  Right side: Invalid tree violating BST property<br>
  Color: Green checkmark for valid, Red X for invalid
</div>

<div class="key-point">
  <strong>Why BST Matters:</strong> The ordering property allows us to eliminate half the tree during search operations, achieving O(log n) time complexity in balanced trees—similar to binary search on sorted arrays but with dynamic insertion and deletion.
</div>

<h2>Core Operations</h2>

<h3>1. Search Operation</h3>

<p>Searching in a BST exploits the ordering property. At each node, compare the target value with the current node's value to decide whether to go left (smaller) or right (larger).</p>

<div class="pseudocode">
<div class="pseudocode-title">SEARCH(node, target):</div>
1. IF node is NULL
2.     RETURN False (value not found)
3. 
4. IF node.data == target
5.     RETURN True (value found)
6. 
7. IF target < node.data
8.     RETURN SEARCH(node.left, target)  // Search left subtree
9. ELSE
10.    RETURN SEARCH(node.right, target) // Search right subtree
11.
12. Time Complexity: O(h) where h is height
13. Best Case: O(log n) for balanced tree
14. Worst Case: O(n) for skewed tree
</div>

<h3>2. Insert Operation</h3>

<p>Insertion maintains the BST property by finding the correct leaf position. Starting from the root, traverse down the tree comparing values until reaching a NULL position where the new node should be inserted.</p>

<div class="pseudocode">
<div class="pseudocode-title">INSERT(node, value):</div>
1. IF node is NULL
2.     CREATE new node with value
3.     RETURN new node
4. 
5. IF value < node.data
6.     node.left = INSERT(node.left, value)  // Insert in left subtree
7. ELSE IF value > node.data
8.     node.right = INSERT(node.right, value) // Insert in right subtree
9. ELSE
10.    // Value already exists, handle duplicates as needed
11.
12. RETURN node
13.
14. Time Complexity: O(h)
15. Space Complexity: O(h) due to recursion stack
</div>

<div class="image-placeholder">
  <strong>IMAGE: BST Insertion Animation</strong><br>
  Step-by-step insertion of values 15, 10, 20, 8, 12, 25<br>
  Show tree growing with each insertion<br>
  Color: Blue for new nodes, Gray for existing
</div>

<h3>3. Delete Operation</h3>

<p>Deletion is the most complex BST operation, with three cases to handle based on the number of children the node has.</p>

<div class="pseudocode">
<div class="pseudocode-title">DELETE(node, value):</div>
1. IF node is NULL
2.     RETURN NULL (value not found)
3. 
4. IF value < node.data
5.     node.left = DELETE(node.left, value)
6. ELSE IF value > node.data
7.     node.right = DELETE(node.right, value)
8. ELSE
9.     // Node to delete found
10.    
11.    CASE 1: Node has no children (leaf)
12.        RETURN NULL
13.    
14.    CASE 2: Node has one child
15.        IF node.left is NULL
16.            RETURN node.right
17.        IF node.right is NULL
18.            RETURN node.left
19.    
20.    CASE 3: Node has two children
21.        Find inorder successor (minimum in right subtree)
22.        Replace node's data with successor's data
23.        DELETE successor from right subtree
24.
25. RETURN node
</div>

<h2>Finding Minimum and Maximum</h2>

<div class="property-box">
  <p><strong>Minimum Value:</strong> Keep going left until you reach the leftmost node (no left child).</p>
  <p><strong>Maximum Value:</strong> Keep going right until you reach the rightmost node (no right child).</p>
  <p>Both operations run in O(h) time where h is the tree height.</p>
</div>

<div class="pseudocode">
<div class="pseudocode-title">FIND_MIN(node):</div>
1. WHILE node.left is NOT NULL
2.     node = node.left
3. RETURN node
<br>
<div class="pseudocode-title">FIND_MAX(node):</div>
1. WHILE node.right is NOT NULL
2.     node = node.right
3. RETURN node
</div>

<h2>BST Traversal Methods</h2>

<p>BSTs can be traversed in multiple ways, each serving different purposes:</p>

<div class="definition-box">
  <p><strong>Inorder Traversal (Left-Root-Right):</strong> Visits nodes in ascending order. Critical property for BST validation.</p>
  <p><strong>Preorder Traversal (Root-Left-Right):</strong> Useful for creating a copy of the tree or prefix expression evaluation.</p>
  <p><strong>Postorder Traversal (Left-Right-Root):</strong> Used for deleting trees or postfix expression evaluation.</p>
</div>

<div class="pseudocode">
<div class="pseudocode-title">INORDER_TRAVERSAL(node):</div>
1. IF node is NOT NULL
2.     INORDER_TRAVERSAL(node.left)
3.     PRINT node.data
4.     INORDER_TRAVERSAL(node.right)
5.
6. For BST, this prints values in sorted order!
</div>

<h2>Time Complexity Analysis</h2>

<table>
  <tr>
    <th>Operation</th>
    <th>Average Case</th>
    <th>Worst Case</th>
  </tr>
  <tr>
    <td>Search</td>
    <td>O(log n)</td>
    <td>O(n)</td>
  </tr>
  <tr>
    <td>Insert</td>
    <td>O(log n)</td>
    <td>O(n)</td>
  </tr>
  <tr>
    <td>Delete</td>
    <td>O(log n)</td>
    <td>O(n)</td>
  </tr>
  <tr>
    <td>Find Min/Max</td>
    <td>O(log n)</td>
    <td>O(n)</td>
  </tr>
  <tr>
    <td>Inorder Traversal</td>
    <td>O(n)</td>
    <td>O(n)</td>
  </tr>
</table>

<div class="warning-box">
  <strong>⚠️ Worst Case Scenario:</strong> When elements are inserted in sorted order (ascending or descending), the BST degenerates into a linked list with height n, making all operations O(n). This is why self-balancing trees (AVL, Red-Black) were invented—they guarantee O(log n) operations by maintaining tree balance.
</div>

<h2>Validating a BST</h2>

<p>A common interview question: How do you verify if a binary tree is a valid BST? Simply checking each node against its children is insufficient—you must ensure the BST property holds for the entire tree.</p>

<div class="pseudocode">
<div class="pseudocode-title">IS_VALID_BST(node, min_value, max_value):</div>
1. IF node is NULL
2.     RETURN True
3. 
4. IF node.data <= min_value OR node.data >= max_value
5.     RETURN False
6. 
7. RETURN IS_VALID_BST(node.left, min_value, node.data) AND
8.        IS_VALID_BST(node.right, node.data, max_value)
9.
10. Initial call: IS_VALID_BST(root, -INFINITY, +INFINITY)
</div>

<h2>Practical Applications</h2>

<ul>
  <li><strong>Database Indexing:</strong> MySQL and PostgreSQL use B-Trees (generalized BSTs) for indexing millions of records</li>
  <li><strong>File Systems:</strong> Directory structures and file organization in operating systems</li>
  <li><strong>Expression Parsing:</strong> Compilers use BSTs to store and evaluate expressions</li>
  <li><strong>Auto-complete:</strong> Search engines use modified BSTs (Tries) for suggestion systems</li>
  <li><strong>Game Development:</strong> BSTs manage game object hierarchies and collision detection</li>
</ul>

<div class="key-point">
  <strong>Interview Tip:</strong> When asked about BST problems, always clarify: Can the tree contain duplicate values? What should happen on duplicate insertion? Are we using 0-indexed or 1-indexed arrays if applicable? These questions show attention to detail!
</div>

<h2>Common Pitfalls</h2>

<ul>
  <li><strong>Invalid BST Check:</strong> Don't just compare a node with its immediate children—use range validation</li>
  <li><strong>Duplicate Handling:</strong> Decide upfront whether duplicates go left, right, or are rejected</li>
  <li><strong>Empty Tree Operations:</strong> Always check for NULL root before operations</li>
  <li><strong>Deletion Complexity:</strong> The two-children case is tricky—practice finding inorder successor/predecessor</li>
</ul>

<h2>Next Steps</h2>

<p>While BSTs provide efficient operations in the average case, their worst-case O(n) complexity is problematic for production systems. Next, you'll learn about <strong>Tree Traversal Algorithms</strong> in depth, followed by <strong>Balanced Trees</strong> (AVL and Red-Black trees) that guarantee O(log n) operations regardless of insertion order.</p>

</body>
</html>