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
    h3 {
      color: #34495e;
      font-size: 18px;
      margin-top: 20px;
      margin-bottom: 10px;
    }
    .intro-box {
      background-color: #ecf0f1;
      padding: 20px;
      border-radius: 6px;
      margin: 20px 0;
      border-left: 4px solid #3498db;
    }
    .problem-box {
      background-color: #fff5e6;
      padding: 18px 20px;
      border-radius: 6px;
      margin: 20px 0;
      border-left: 4px solid #e67e22;
    }
    .problem-box h3 {
      color: #d35400;
      margin-top: 0;
    }
    .approach-box {
      background-color: #e8f4f8;
      padding: 15px 20px;
      border-radius: 6px;
      margin: 15px 0;
      border-left: 4px solid #3498db;
    }
    .optimal-box {
      background-color: #e8f8e8;
      padding: 15px 20px;
      border-radius: 6px;
      margin: 15px 0;
      border-left: 4px solid #27ae60;
    }
    .pattern-box {
      background-color: #f3e5f5;
      padding: 15px 20px;
      border-radius: 6px;
      margin: 15px 0;
      border-left: 4px solid #9b59b6;
    }
    .key-point {
      background-color: #fff9e6;
      padding: 15px 20px;
      border-radius: 6px;
      margin: 15px 0;
      border-left: 4px solid #f39c12;
    }
    .complexity-note {
      background-color: #ffeef0;
      padding: 12px 16px;
      border-radius: 6px;
      margin: 10px 0;
      font-size: 14px;
      border-left: 3px solid #e74c3c;
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
    .pattern-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 15px;
      margin: 20px 0;
    }
    .pattern-card {
      background: #f8f9fa;
      padding: 15px;
      border-radius: 6px;
      border: 2px solid #3498db;
    }
    .pattern-card h4 {
      color: #3498db;
      margin-top: 0;
      font-size: 16px;
    }
  </style>
</head>
<body>

<div class="lesson-meta">
  Unit 1.1: Binary Trees and Binary Search Trees | Lesson 4 of 4
</div>

<h1>Binary Tree Problems</h1>

<div class="intro-box">
  <p>Binary tree problems are among the most frequently asked questions in FAANG and product-based company interviews. These problems test your understanding of recursion, tree traversal, and algorithmic thinking. Success requires recognizing patterns, choosing the right traversal approach, and optimizing from brute force to efficient solutions.</p>
  
  <p>This lesson covers classic problems with multiple approaches—from intuitive brute force to optimal solutions. You'll learn to identify patterns, understand complexity trade-offs, and develop problem-solving strategies used by top engineers.</p>
</div>

<h2>Common Problem-Solving Patterns</h2>

<div class="pattern-grid">
  <div class="pattern-card">
    <h4>Recursive DFS</h4>
    <p>Break problem into subproblems on left and right subtrees. Combine results at each node.</p>
    <p><em>Problems:</em> Height, diameter, path sums</p>
  </div>
  
  <div class="pattern-card">
    <h4>Level Order (BFS)</h4>
    <p>Process nodes level by level using a queue. Track level information.</p>
    <p><em>Problems:</em> Level averages, zigzag traversal, right side view</p>
  </div>
  
  <div class="pattern-card">
    <h4>Two Pointer / Path</h4>
    <p>Track paths from root to nodes. Compare or manipulate paths.</p>
    <p><em>Problems:</em> LCA, path sum, root to leaf paths</p>
  </div>
  
  <div class="pattern-card">
    <h4>Post-order Processing</h4>
    <p>Process children before parent. Build up from leaves.</p>
    <p><em>Problems:</em> Tree serialization, subtree validation</p>
  </div>
</div>

<h2>Problem 1: Maximum Depth of Binary Tree</h2>

<div class="problem-box">
  <h3>Problem Statement</h3>
  <p>Given the root of a binary tree, return its maximum depth. The maximum depth is the number of nodes along the longest path from the root to the farthest leaf node.</p>
  <p><strong>Example:</strong> For tree [3,9,20,null,null,15,7], output is 3</p>
  <p><strong>Companies:</strong> Amazon, Microsoft, Google, Facebook</p>
</div>

<div class="image-placeholder">
  <strong>IMAGE: Max Depth Example</strong><br>
  Tree showing depth calculation from root to deepest leaf<br>
  Highlight the longest path with different color<br>
  Color: Blue nodes, Red path highlighting
</div>

<h3>Approach 1: Brute Force (Generate All Paths)</h3>

<div class="approach-box">
  <p><strong>Idea:</strong> Generate all root-to-leaf paths and find the longest one.</p>
  <p><strong>Method:</strong> Use DFS to collect all paths, then iterate to find maximum length.</p>
</div>

<div class="complexity-note">
  <strong>Time:</strong> O(n²) - O(n) to generate paths + O(n) to find max for each<br>
  <strong>Space:</strong> O(n²) - storing all paths<br>
  <strong>Issue:</strong> Unnecessary space usage and extra iteration
</div>

<h3>Approach 2: Optimal (Recursive DFS)</h3>

<div class="optimal-box">
  <p><strong>Insight:</strong> Max depth = 1 + maximum of (left subtree depth, right subtree depth)</p>
  <p><strong>Pattern:</strong> Recursive divide-and-conquer with base case</p>
</div>

<div class="pseudocode">
<div class="pseudocode-title">MAX_DEPTH(node):</div>
1. IF node is NULL
2.     RETURN 0
3. 
4. left_depth = MAX_DEPTH(node.left)
5. right_depth = MAX_DEPTH(node.right)
6. 
7. RETURN 1 + MAX(left_depth, right_depth)
8.
9. Time: O(n) - visit each node once
10. Space: O(h) - recursion stack height
</div>

<div class="key-point">
  <strong>Pattern Recognition:</strong> When a problem asks for tree metrics (height, depth, size), think recursive DFS where each node's answer depends on its children's answers.
</div>

<h2>Problem 2: Diameter of Binary Tree</h2>

<div class="problem-box">
  <h3>Problem Statement</h3>
  <p>The diameter of a binary tree is the length of the longest path between any two nodes. This path may or may not pass through the root.</p>
  <p><strong>Example:</strong> For tree [1,2,3,4,5], diameter is 3 (path: 4→2→1→3)</p>
  <p><strong>Companies:</strong> Google, Amazon, Facebook, Microsoft</p>
</div>

<h3>Approach 1: Brute Force (Calculate Height at Each Node)</h3>

<div class="approach-box">
  <p><strong>Idea:</strong> For each node, diameter through it = left height + right height. Find maximum across all nodes.</p>
  <p><strong>Method:</strong> Call height function separately for each node's left and right subtrees.</p>
</div>

<div class="complexity-note">
  <strong>Time:</strong> O(n²) - For each of n nodes, calculate height O(n)<br>
  <strong>Space:</strong> O(h)<br>
  <strong>Issue:</strong> Redundant height calculations for same subtrees
</div>

<h3>Approach 2: Optimal (Single Pass DFS)</h3>

<div class="optimal-box">
  <p><strong>Insight:</strong> Calculate diameter and height simultaneously in one pass using global variable to track maximum diameter.</p>
  <p><strong>Optimization:</strong> Each subtree's height is computed only once.</p>
</div>

<div class="pseudocode">
<div class="pseudocode-title">DIAMETER_HELPER(node, max_diameter):</div>
1. IF node is NULL
2.     RETURN 0
3. 
4. left_height = DIAMETER_HELPER(node.left, max_diameter)
5. right_height = DIAMETER_HELPER(node.right, max_diameter)
6. 
7. // Diameter through current node
8. current_diameter = left_height + right_height
9. max_diameter = MAX(max_diameter, current_diameter)
10.
11. // Return height for parent's calculation
12. RETURN 1 + MAX(left_height, right_height)
13.
14. Time: O(n) - single pass
15. Space: O(h) - recursion stack
</div>

<div class="key-point">
  <strong>Optimization Technique:</strong> When you need multiple metrics (height, diameter), compute them together in one traversal rather than separate passes. Use helper variables to track global metrics.
</div>

<h2>Problem 3: Lowest Common Ancestor (LCA)</h2>

<div class="problem-box">
  <h3>Problem Statement</h3>
  <p>Given a binary tree and two nodes p and q, find their lowest common ancestor. LCA is the lowest node that has both p and q as descendants (a node can be a descendant of itself).</p>
  <p><strong>Example:</strong> For tree [3,5,1,6,2,0,8] with p=5, q=1, LCA is 3</p>
  <p><strong>Companies:</strong> Facebook, Amazon, Microsoft, LinkedIn</p>
</div>

<div class="image-placeholder">
  <strong>IMAGE: LCA Visualization</strong><br>
  Tree showing two nodes and their lowest common ancestor<br>
  Highlight paths from root to both nodes<br>
  Color: Green for target nodes, Blue for LCA
</div>

<h3>Approach 1: Store Paths and Compare</h3>

<div class="approach-box">
  <p><strong>Idea:</strong> Find path from root to p and root to q. The last common node in both paths is the LCA.</p>
  <p><strong>Method:</strong> Use two separate DFS calls to store paths, then compare arrays.</p>
</div>

<div class="complexity-note">
  <strong>Time:</strong> O(n) - two DFS traversals + path comparison<br>
  <strong>Space:</strong> O(h) - two path arrays<br>
  <strong>Issue:</strong> Requires extra space and two passes
</div>

<h3>Approach 2: Optimal (Single Pass Recursive)</h3>

<div class="optimal-box">
  <p><strong>Insight:</strong> If current node is p or q, return it. If both subtrees return non-null, current node is LCA. If only one returns non-null, propagate it up.</p>
  <p><strong>Pattern:</strong> Bottom-up information passing through return values.</p>
</div>

<div class="pseudocode">
<div class="pseudocode-title">FIND_LCA(node, p, q):</div>
1. IF node is NULL OR node == p OR node == q
2.     RETURN node
3. 
4. left = FIND_LCA(node.left, p, q)
5. right = FIND_LCA(node.right, p, q)
6. 
7. // Both found in different subtrees - current node is LCA
8. IF left is NOT NULL AND right is NOT NULL
9.     RETURN node
10.
11. // One found, return that subtree's result
12. RETURN (left is NOT NULL) ? left : right
13.
14. Time: O(n) - single traversal
15. Space: O(h) - recursion stack
</div>

<h2>Problem 4: Path Sum (Root to Leaf)</h2>

<div class="problem-box">
  <h3>Problem Statement</h3>
  <p>Given a binary tree and a target sum, determine if there exists a root-to-leaf path where the sum of node values equals the target.</p>
  <p><strong>Example:</strong> For tree [5,4,8,11,null,13,4,7,2,null,null,null,1] and sum=22, return true (path: 5→4→11→2)</p>
  <p><strong>Companies:</strong> Amazon, Google, Microsoft, Apple</p>
</div>

<h3>Approach 1: Generate All Paths</h3>

<div class="approach-box">
  <p><strong>Idea:</strong> Generate all root-to-leaf paths, then check each path sum.</p>
  <p><strong>Method:</strong> DFS to collect paths in arrays, iterate to check sums.</p>
</div>

<div class="complexity-note">
  <strong>Time:</strong> O(n²) - generate paths + check sums<br>
  <strong>Space:</strong> O(n²) - storing all paths<br>
  <strong>Issue:</strong> Excessive memory usage
</div>

<h3>Approach 2: Optimal (Subtract and Track)</h3>

<div class="optimal-box">
  <p><strong>Insight:</strong> Subtract current node value from target and pass remaining sum to children. At leaf, check if remaining sum equals leaf value.</p>
  <p><strong>Pattern:</strong> Top-down accumulation with early termination.</p>
</div>

<div class="pseudocode">
<div class="pseudocode-title">HAS_PATH_SUM(node, remaining_sum):</div>
1. IF node is NULL
2.     RETURN False
3. 
4. // Check if leaf node with matching sum
5. IF node.left is NULL AND node.right is NULL
6.     RETURN (remaining_sum == node.data)
7. 
8. // Subtract current value and check children
9. new_sum = remaining_sum - node.data
10. 
11. RETURN HAS_PATH_SUM(node.left, new_sum) OR
12.        HAS_PATH_SUM(node.right, new_sum)
13.
14. Time: O(n) - visit each node once
15. Space: O(h) - recursion stack
</div>

<div class="pattern-box">
  <strong>Top-Down Pattern:</strong> When tracking cumulative values (sum, product, path), pass modified values down to children rather than collecting and checking later. This enables early termination and reduces space.
</div>

<h2>Problem 5: Symmetric Tree</h2>

<div class="problem-box">
  <h3>Problem Statement</h3>
  <p>Check if a binary tree is a mirror of itself (i.e., symmetric around its center).</p>
  <p><strong>Example:</strong> Tree [1,2,2,3,4,4,3] is symmetric; [1,2,2,null,3,null,3] is not</p>
  <p><strong>Companies:</strong> Microsoft, Amazon, LinkedIn, Bloomberg</p>
</div>

<h3>Approach: Compare Mirror Subtrees</h3>

<div class="optimal-box">
  <p><strong>Insight:</strong> A tree is symmetric if left subtree is mirror of right subtree. Two trees are mirrors if their roots match and left of one equals right of other.</p>
  <p><strong>Pattern:</strong> Simultaneous traversal of two subtrees with mirrored logic.</p>
</div>

<div class="pseudocode">
<div class="pseudocode-title">IS_MIRROR(left, right):</div>
1. IF left is NULL AND right is NULL
2.     RETURN True
3. 
4. IF left is NULL OR right is NULL
5.     RETURN False
6. 
7. // Check current nodes and mirror subtrees
8. RETURN (left.data == right.data) AND
9.        IS_MIRROR(left.left, right.right) AND
10.       IS_MIRROR(left.right, right.left)
11.
12. IS_SYMMETRIC(root):
13.     RETURN IS_MIRROR(root.left, root.right)
14.
15. Time: O(n) - visit all nodes
16. Space: O(h) - recursion depth
</div>

<h2>Problem 6: Vertical Order Traversal</h2>

<div class="problem-box">
  <h3>Problem Statement</h3>
  <p>Given a binary tree, return the vertical order traversal of its nodes' values. Nodes in the same column and row should be ordered by their values.</p>
  <p><strong>Example:</strong> For tree [3,9,20,null,null,15,7], return [[9],[3,15],[20],[7]]</p>
  <p><strong>Companies:</strong> Facebook, Google, Amazon</p>
</div>

<h3>Approach: Level Order with Column Tracking</h3>

<div class="optimal-box">
  <p><strong>Insight:</strong> Use BFS with column index. Root at column 0, left child at col-1, right child at col+1. Group nodes by column and sort by row then value.</p>
  <p><strong>Pattern:</strong> Modified BFS with additional coordinate tracking.</p>
</div>

<div class="pseudocode">
<div class="pseudocode-title">VERTICAL_ORDER(root):</div>
1. IF root is NULL
2.     RETURN empty list
3. 
4. CREATE map: column -> list of (row, value)
5. CREATE queue: (node, row, column)
6. ENQUEUE(queue, (root, 0, 0))
7. 
8. WHILE queue is NOT empty
9.     (node, row, col) = DEQUEUE(queue)
10.    ADD (row, node.data) to map[col]
11.    
12.    IF node.left exists
13.        ENQUEUE(queue, (node.left, row+1, col-1))
14.    IF node.right exists
15.        ENQUEUE(queue, (node.right, row+1, col+1))
16.
17. SORT each column's list by row, then by value
18. RETURN columns in sorted order
19.
20. Time: O(n log n) - sorting nodes
21. Space: O(n) - map and queue
</div>

<h2>Key Problem-Solving Strategies</h2>

<ul>
  <li><strong>Identify the Pattern:</strong> Is it asking for paths? Use DFS. Level-wise information? Use BFS. Subtree property? Use recursion.</li>
  <li><strong>Choose Traversal:</strong> Inorder for BST problems, Postorder for bottom-up processing, Preorder for top-down, Level-order for breadth-first requirements.</li>
  <li><strong>Optimize Space:</strong> Use return values instead of global arrays. Process during traversal instead of collecting then processing.</li>
  <li><strong>Handle Edge Cases:</strong> Always check for null trees, single nodes, and unbalanced structures.</li>
  <li><strong>Draw Examples:</strong> Sketch small trees (3-5 nodes) to understand the pattern before coding.</li>
</ul>

<div class="key-point">
  <strong>Interview Success Formula:</strong> Start with brute force explanation to show understanding. Identify inefficiency. Propose optimization. Code the optimal solution. Discuss trade-offs. Handle edge cases. This structured approach impresses interviewers even if you don't reach the optimal solution immediately.
</div>

<h2>Next Steps</h2>

<p>You've now mastered binary tree fundamentals and problem-solving patterns. Next, explore <strong>Balanced Trees (AVL Trees)</strong> to understand how self-balancing mechanisms guarantee O(log n) operations regardless of insertion order—crucial for building robust production systems.</p>

</body>
</html>