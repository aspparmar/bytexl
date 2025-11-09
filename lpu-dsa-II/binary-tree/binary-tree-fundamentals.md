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
    .terminology-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 15px;
      margin: 20px 0;
    }
    .term-card {
      background: #f8f9fa;
      padding: 15px;
      border-radius: 6px;
      border: 1px solid #dee2e6;
    }
    .term-card strong {
      color: #3498db;
      font-size: 16px;
      display: block;
      margin-bottom: 8px;
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
    .code-reference {
      background: #2c3e50;
      color: #ecf0f1;
      padding: 12px 16px;
      border-radius: 6px;
      margin: 15px 0;
      font-family: 'Courier New', monospace;
      font-size: 14px;
    }
    ul, ol {
      margin: 15px 0;
      padding-left: 30px;
    }
    li {
      margin: 8px 0;
    }
  </style>
</head>
<body>

<div class="lesson-meta">
  Unit 1.1: Binary Trees and Binary Search Trees | Lesson 1 of 4
</div>

<h1>Binary Tree Fundamentals</h1>

<div class="intro-box">
  <p><strong>Binary trees</strong> are hierarchical data structures where each node has at most two children, referred to as the left child and right child. They are fundamental building blocks for advanced data structures like Binary Search Trees (BST), AVL Trees, Red-Black Trees, and Heaps.</p>
  
  <p>Binary trees power critical applications: file systems use them for directory organization, databases rely on B-Trees for indexing, compilers build expression trees for parsing, and machine learning uses decision trees for classification.</p>
</div>

<h2>Why Binary Trees Matter</h2>

<p>Binary trees provide an efficient way to organize hierarchical data with O(log n) access time in balanced scenarios. Unlike arrays with O(n) search time or linked lists that can't perform binary search, balanced binary trees combine the best of both worlds—dynamic size with logarithmic operations.</p>

<div class="key-point">
  <strong>Real-World Impact:</strong> Google's search indexing, MongoDB's data storage, and network routing protocols all leverage tree structures for performance. Understanding binary trees is essential for any software engineer working with hierarchical data or optimization problems.
</div>

<h2>Core Terminology</h2>

<div class="terminology-grid">
  <div class="term-card">
    <strong>Node</strong>
    <p>The fundamental unit containing data and references to at most two children (left and right).</p>
  </div>
  
  <div class="term-card">
    <strong>Root</strong>
    <p>The topmost node with no parent. Every tree has exactly one root, serving as the entry point.</p>
  </div>
  
  <div class="term-card">
    <strong>Leaf (Terminal Node)</strong>
    <p>A node with no children. Both left and right pointers are null.</p>
  </div>
  
  <div class="term-card">
    <strong>Parent & Child</strong>
    <p>If node A points to node B, then A is the parent and B is the child. Each node has at most one parent.</p>
  </div>
  
  <div class="term-card">
    <strong>Height</strong>
    <p>The length of the longest path from a node to a leaf. Empty tree has height -1.</p>
  </div>
  
  <div class="term-card">
    <strong>Depth (Level)</strong>
    <p>The distance from the root to a node. Root has depth 0.</p>
  </div>
</div>

<h2>Types of Binary Trees</h2>

<div class="definition-box">
  <p><strong>Full Binary Tree:</strong> Every node has either 0 or 2 children. No node has exactly one child.</p>
  <p><em>Property:</em> If n internal nodes exist, there are n+1 leaves.</p>
  <p><em>Use Case:</em> Huffman coding trees for data compression.</p>
</div>

<div class="definition-box">
  <p><strong>Complete Binary Tree:</strong> All levels are fully filled except possibly the last level, which fills from left to right.</p>
  <p><em>Property:</em> Height is ⌊log₂(n)⌋ where n is the number of nodes.</p>
  <p><em>Use Case:</em> Binary heaps in priority queues (Dijkstra's algorithm, job scheduling).</p>
</div>

<div class="definition-box">
  <p><strong>Perfect Binary Tree:</strong> All internal nodes have exactly two children, and all leaves are at the same level.</p>
  <p><em>Property:</em> Total nodes = 2^(h+1) - 1 where h is height.</p>
  <p><em>Use Case:</em> Segment trees for range queries, tournament brackets.</p>
</div>

<div class="definition-box">
  <p><strong>Balanced Binary Tree:</strong> The height difference between left and right subtrees is at most 1 for every node.</p>
  <p><em>Property:</em> Guarantees O(log n) operations.</p>
  <p><em>Use Case:</em> AVL trees and Red-Black trees in database indexing systems.</p>
</div>

<div class="definition-box">
  <p><strong>Degenerate (Skewed) Tree:</strong> Each parent has exactly one child, essentially forming a linked list.</p>
  <p><em>Property:</em> Height = n-1, worst case for operations O(n).</p>
  <p><em>Anti-Pattern:</em> Occurs when inserting sorted data without balancing.</p>
</div>

<h2>Basic Node Structure</h2>

<div class="image-placeholder">
  <strong>IMAGE: Binary Tree Node Structure Diagram</strong><br>
  Show a node with three components: Data, Left Pointer, Right Pointer<br>
  Color: Light blue boxes with arrows
</div>

<div class="code-reference">
  <strong>CODE BLOCK 1: Python TreeNode Implementation</strong><br>
  [Insert iframe with TreeNode class definition]
</div>

<h2>Visual Example</h2>

<div class="image-placeholder">
  <strong>IMAGE: Sample Binary Tree</strong><br>
  Tree structure with nodes 1,2,3,4,5<br>
  Root: 1, Children: 2,3, Grandchildren: 4,5<br>
  Color: Blue nodes with black connecting lines
</div>

<h2>Essential Operations</h2>

<p>Three fundamental operations form the foundation of binary tree algorithms:</p>

<ol>
  <li><strong>Height Calculation:</strong> Recursively find the maximum depth from root to any leaf. Time: O(n), Space: O(h).</li>
  <li><strong>Node Count:</strong> Traverse entire tree counting each node. Time: O(n), Space: O(h).</li>
  <li><strong>Leaf Count:</strong> Count nodes with no children. Time: O(n), Space: O(h).</li>
</ol>

<div class="code-reference">
  <strong>CODE BLOCK 2: Essential Tree Operations</strong><br>
  [Insert iframe with height(), count_nodes(), count_leaves() functions]
</div>

<h2>Key Properties & Formulas</h2>

<ul>
  <li><strong>Maximum nodes at level L:</strong> 2^L</li>
  <li><strong>Maximum nodes in tree of height h:</strong> 2^(h+1) - 1</li>
  <li><strong>Minimum height for n nodes:</strong> ⌈log₂(n+1)⌉ - 1</li>
  <li><strong>In a full binary tree:</strong> Leaves = Internal Nodes + 1</li>
  <li><strong>Array representation:</strong> Left child at 2i+1, Right child at 2i+2, Parent at ⌊(i-1)/2⌋</li>
</ul>

<div class="key-point">
  <strong>Interview Tip:</strong> Always clarify whether the tree can be empty, if it contains duplicate values, and the expected size. This demonstrates thorough thinking and helps avoid edge case bugs!
</div>

<h2>Common Pitfalls</h2>

<ul>
  <li><strong>Null/Empty Trees:</strong> Always check if root is null before operations to prevent crashes.</li>
  <li><strong>Height vs Depth Confusion:</strong> Height is bottom-up (node to leaf), depth is top-down (root to node).</li>
  <li><strong>Stack Overflow:</strong> Deep recursive calls on skewed trees can cause stack overflow. Consider iterative approaches for production.</li>
  <li><strong>Off-by-One Errors:</strong> Remember: empty tree height is -1, single node height is 0.</li>
</ul>

<h2>Next Steps</h2>

<p>Now that you understand binary tree fundamentals, you're ready to explore <strong>Binary Search Trees (BST)</strong>, which add an ordering property that enables efficient searching, insertion, and deletion in O(log n) time for balanced trees.</p>

</body>
</html>