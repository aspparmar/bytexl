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
    .comparison-box {
      background-color: #f0f8f0;
      padding: 15px 20px;
      border-radius: 6px;
      margin: 15px 0;
      border-left: 4px solid #27ae60;
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
    .traversal-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 15px;
      margin: 20px 0;
    }
    .traversal-card {
      background: #f8f9fa;
      padding: 15px;
      border-radius: 6px;
      border: 2px solid #dee2e6;
    }
    .traversal-card h3 {
      color: #3498db;
      margin-top: 0;
      font-size: 18px;
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
  Unit 1.1: Binary Trees and Binary Search Trees | Lesson 3 of 4
</div>

<h1>Tree Traversal Algorithms</h1>

<div class="intro-box">
  <p><strong>Tree traversal</strong> is the process of visiting each node in a tree exactly once in a systematic way. Unlike linear data structures (arrays, linked lists) that have a single logical way to traverse, trees can be traversed in multiple ways depending on the order in which nodes are visited.</p>
  
  <p>Traversal algorithms are fundamental to tree operations: searching for values, printing tree contents, evaluating expressions, serializing trees for storage, and validating tree properties. Mastering these patterns is essential for solving complex tree problems in interviews and real-world applications.</p>
</div>

<h2>Why Traversal Order Matters</h2>

<p>Different traversal orders serve different purposes. Inorder traversal of a BST yields sorted data, preorder traversal helps in creating tree copies, postorder traversal is used for tree deletion, and level-order traversal finds shortest paths. Understanding when to use each traversal is key to efficient problem-solving.</p>

<div class="image-placeholder">
  <strong>IMAGE: Sample Tree for All Examples</strong><br>
  Tree structure: Root 1, Children 2 and 3, Grandchildren 4,5,6,7<br>
  Use this same tree to show all traversal outputs<br>
  Color: Blue nodes with numbered labels
</div>

<h2>Depth-First Traversals</h2>

<p>Depth-First Search (DFS) explores as far down a branch as possible before backtracking. There are three main DFS traversal orders, differing only in when the root is processed relative to its subtrees.</p>

<h3>1. Inorder Traversal (Left-Root-Right)</h3>

<div class="definition-box">
  <p><strong>Order:</strong> Visit left subtree → Process current node → Visit right subtree</p>
  <p><strong>Key Property:</strong> For BST, produces nodes in ascending sorted order</p>
  <p><strong>Applications:</strong> BST validation, retrieving sorted data, expression tree evaluation</p>
</div>

<div class="pseudocode">
<div class="pseudocode-title">INORDER(node):</div>
1. IF node is NULL
2.     RETURN
3. 
4. INORDER(node.left)        // Visit left subtree first
5. PROCESS(node.data)         // Process current node
6. INORDER(node.right)        // Visit right subtree last
7.
8. Time Complexity: O(n) - visits each node once
9. Space Complexity: O(h) - recursion stack depth
10.
11. Example Output for tree [1,2,3,4,5,6,7]: 4,2,5,1,6,3,7
</div>

<h3>2. Preorder Traversal (Root-Left-Right)</h3>

<div class="definition-box">
  <p><strong>Order:</strong> Process current node → Visit left subtree → Visit right subtree</p>
  <p><strong>Key Property:</strong> Root is always processed first, useful for tree copying</p>
  <p><strong>Applications:</strong> Creating tree copies, prefix expression evaluation, serialization</p>
</div>

<div class="pseudocode">
<div class="pseudocode-title">PREORDER(node):</div>
1. IF node is NULL
2.     RETURN
3. 
4. PROCESS(node.data)          // Process current node first
5. PREORDER(node.left)         // Visit left subtree
6. PREORDER(node.right)        // Visit right subtree
7.
8. Time Complexity: O(n)
9. Space Complexity: O(h)
10.
11. Example Output for tree [1,2,3,4,5,6,7]: 1,2,4,5,3,6,7
</div>

<h3>3. Postorder Traversal (Left-Right-Root)</h3>

<div class="definition-box">
  <p><strong>Order:</strong> Visit left subtree → Visit right subtree → Process current node</p>
  <p><strong>Key Property:</strong> Root is processed last, children before parent</p>
  <p><strong>Applications:</strong> Tree deletion, postfix expression evaluation, calculating directory sizes</p>
</div>

<div class="pseudocode">
<div class="pseudocode-title">POSTORDER(node):</div>
1. IF node is NULL
2.     RETURN
3. 
4. POSTORDER(node.left)        // Visit left subtree
5. POSTORDER(node.right)       // Visit right subtree
6. PROCESS(node.data)          // Process current node last
7.
8. Time Complexity: O(n)
9. Space Complexity: O(h)
10.
11. Example Output for tree [1,2,3,4,5,6,7]: 4,5,2,6,7,3,1
</div>

<div class="image-placeholder">
  <strong>IMAGE: DFS Traversal Comparison</strong><br>
  Three side-by-side trees showing visit order for Inorder, Preorder, Postorder<br>
  Number each node with visit sequence (1st, 2nd, 3rd...)<br>
  Color: Different color for each traversal type
</div>

<h2>Breadth-First Traversal (Level Order)</h2>

<p>Breadth-First Search (BFS) visits nodes level by level, from left to right. Unlike DFS which uses recursion (implicit stack), BFS uses an explicit queue data structure.</p>

<div class="definition-box">
  <p><strong>Order:</strong> Visit all nodes at depth d before visiting nodes at depth d+1</p>
  <p><strong>Key Property:</strong> Finds shortest path in unweighted trees</p>
  <p><strong>Applications:</strong> Finding tree width, level-order printing, finding nodes at distance k</p>
</div>

<div class="pseudocode">
<div class="pseudocode-title">LEVEL_ORDER(root):</div>
1. IF root is NULL
2.     RETURN
3. 
4. CREATE empty queue Q
5. ENQUEUE(Q, root)
6. 
7. WHILE Q is NOT empty
8.     node = DEQUEUE(Q)
9.     PROCESS(node.data)
10.    
11.    IF node.left is NOT NULL
12.        ENQUEUE(Q, node.left)
13.    IF node.right is NOT NULL
14.        ENQUEUE(Q, node.right)
15.
16. Time Complexity: O(n)
17. Space Complexity: O(w) where w is maximum width
18.
19. Example Output for tree [1,2,3,4,5,6,7]: 1,2,3,4,5,6,7
</div>

<div class="key-point">
  <strong>Queue vs Stack:</strong> BFS uses a queue (FIFO) to process nodes level by level, while DFS uses a stack (LIFO) either explicitly or through recursion. This fundamental difference determines the order of node processing.
</div>

<h2>Iterative DFS Using Stack</h2>

<p>While DFS is naturally recursive, it can also be implemented iteratively using an explicit stack. This is useful to avoid stack overflow on very deep trees.</p>

<div class="pseudocode">
<div class="pseudocode-title">ITERATIVE_PREORDER(root):</div>
1. IF root is NULL
2.     RETURN
3. 
4. CREATE empty stack S
5. PUSH(S, root)
6. 
7. WHILE S is NOT empty
8.     node = POP(S)
9.     PROCESS(node.data)
10.    
11.    // Push right first so left is processed first
12.    IF node.right is NOT NULL
13.        PUSH(S, node.right)
14.    IF node.left is NOT NULL
15.        PUSH(S, node.left)
16.
17. Space Complexity: O(h) for stack storage
</div>

<h2>Traversal Comparison</h2>

<table>
  <tr>
    <th>Traversal</th>
    <th>Order</th>
    <th>Data Structure</th>
    <th>Primary Use Case</th>
  </tr>
  <tr>
    <td>Inorder</td>
    <td>Left-Root-Right</td>
    <td>Recursion/Stack</td>
    <td>Get sorted data from BST</td>
  </tr>
  <tr>
    <td>Preorder</td>
    <td>Root-Left-Right</td>
    <td>Recursion/Stack</td>
    <td>Copy tree, serialize tree</td>
  </tr>
  <tr>
    <td>Postorder</td>
    <td>Left-Right-Root</td>
    <td>Recursion/Stack</td>
    <td>Delete tree, calculate sizes</td>
  </tr>
  <tr>
    <td>Level Order</td>
    <td>Level by level</td>
    <td>Queue</td>
    <td>Find shortest path, print levels</td>
  </tr>
</table>

<h2>Practical Applications</h2>

<div class="traversal-grid">
  <div class="traversal-card">
    <h3>Expression Trees</h3>
    <p><strong>Inorder:</strong> Produces infix notation (a + b)</p>
    <p><strong>Preorder:</strong> Produces prefix notation (+ a b)</p>
    <p><strong>Postorder:</strong> Produces postfix notation (a b +)</p>
  </div>
  
  <div class="traversal-card">
    <h3>File Systems</h3>
    <p><strong>Preorder:</strong> List directories before contents</p>
    <p><strong>Postorder:</strong> Calculate directory sizes (children before parent)</p>
    <p><strong>Level Order:</strong> Show directory depth structure</p>
  </div>
  
  <div class="traversal-card">
    <h3>Binary Search Trees</h3>
    <p><strong>Inorder:</strong> Retrieve sorted elements</p>
    <p><strong>Preorder:</strong> Validate BST property</p>
    <p><strong>Level Order:</strong> Find kth smallest at level</p>
  </div>
</div>

<h2>Advanced Traversal Techniques</h2>

<div class="comparison-box">
  <p><strong>Morris Traversal:</strong> Inorder/Preorder traversal with O(1) space by temporarily modifying tree structure using threaded pointers. Nodes are connected and disconnected during traversal.</p>
  <p><strong>Reverse Level Order:</strong> Process nodes from bottom to top, right to left. Useful for printing tree upside down or bottom-up calculations.</p>
  <p><strong>Zigzag Traversal:</strong> Alternate left-to-right and right-to-left at each level. Used in spiral printing and specific tree visualizations.</p>
</div>

<h2>Common Interview Problems</h2>

<ul>
  <li><strong>Print nodes at distance K:</strong> Use level-order traversal with depth tracking</li>
  <li><strong>Check if two trees are identical:</strong> Any DFS traversal comparing node by node</li>
  <li><strong>Serialize and deserialize tree:</strong> Preorder traversal with null markers</li>
  <li><strong>Find vertical order of nodes:</strong> Modified level-order with column tracking</li>
  <li><strong>Print boundary of tree:</strong> Combination of left boundary, leaves, and right boundary</li>
</ul>

<div class="key-point">
  <strong>Interview Tip:</strong> When asked to traverse a tree, always clarify: Do you need recursive or iterative solution? Should null nodes be included? What should be the output format? These details matter for correctness!
</div>

<h2>Space Complexity Considerations</h2>

<ul>
  <li><strong>Recursive DFS:</strong> O(h) space for call stack, where h = height. Worst case O(n) for skewed trees.</li>
  <li><strong>Iterative DFS:</strong> O(h) space for explicit stack storage.</li>
  <li><strong>Level Order BFS:</strong> O(w) space for queue, where w = maximum width. Worst case O(n) for complete trees at last level.</li>
  <li><strong>Morris Traversal:</strong> O(1) space but modifies tree temporarily (not suitable for concurrent access).</li>
</ul>

<h2>Next Steps</h2>

<p>Now that you've mastered traversal algorithms, you're ready to tackle <strong>Binary Tree Problems</strong>, where you'll apply these traversal techniques to solve complex challenges like finding paths, calculating depths, and detecting tree properties. These problems are frequently asked in technical interviews at top tech companies.</p>

</body>
</html>