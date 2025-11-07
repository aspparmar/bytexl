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
    .header {
      border-bottom: 3px solid #3498db;
      padding-bottom: 15px;
      margin-bottom: 30px;
    }
    .lesson-meta {
      color: #7f8c8d;
      font-size: 14px;
      margin-bottom: 8px;
    }
    h1 {
      color: #2c3e50;
      font-size: 32px;
      margin: 10px 0;
      font-weight: 600;
    }
    h2 {
      color: #2c3e50;
      font-size: 24px;
      margin-top: 35px;
      margin-bottom: 15px;
      font-weight: 600;
    }
    .intro-text {
      background-color: #ecf0f1;
      padding: 20px;
      border-radius: 8px;
      margin: 20px 0;
      font-size: 16px;
    }
    .flashcards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 15px;
      margin: 25px 0;
    }
    .flashcard {
      background: #3498db;
      color: white;
      padding: 20px;
      border-radius: 8px;
      cursor: pointer;
      min-height: 120px;
      transition: transform 0.3s, box-shadow 0.3s;
      position: relative;
    }
    .flashcard:hover {
      transform: translateY(-5px);
      box-shadow: 0 5px 15px rgba(52, 152, 219, 0.3);
    }
    .flashcard h3 {
      margin: 0 0 10px 0;
      font-size: 18px;
      color: white;
    }
    .flashcard p {
      margin: 0;
      font-size: 14px;
      line-height: 1.5;
    }
    .expandable {
      background: #f8f9fa;
      border: 1px solid #dee2e6;
      border-radius: 8px;
      margin: 15px 0;
      overflow: hidden;
    }
    .expandable-header {
      background: #e9ecef;
      padding: 15px 20px;
      cursor: pointer;
      font-weight: 600;
      display: flex;
      justify-content: space-between;
      align-items: center;
      user-select: none;
    }
    .expandable-header:hover {
      background: #dee2e6;
    }
    .expandable-content {
      padding: 20px;
      display: none;
    }
    .expandable-content.active {
      display: block;
    }
    .arrow {
      transition: transform 0.3s;
    }
    .arrow.rotated {
      transform: rotate(180deg);
    }
    code {
      background: #f4f4f4;
      padding: 2px 6px;
      border-radius: 3px;
      font-family: 'Courier New', monospace;
      font-size: 14px;
    }
    .code-block {
      background: #2c3e50;
      color: #ecf0f1;
      padding: 15px;
      border-radius: 8px;
      overflow-x: auto;
      margin: 15px 0;
      font-family: 'Courier New', monospace;
      font-size: 13px;
      line-height: 1.5;
    }
    .tree-visual {
      text-align: center;
      font-family: 'Courier New', monospace;
      background: #f8f9fa;
      padding: 20px;
      border-radius: 8px;
      margin: 20px 0;
      font-size: 14px;
      line-height: 1.8;
    }
    .continue-btn {
      background: #3498db;
      color: white;
      padding: 12px 30px;
      border: none;
      border-radius: 5px;
      font-size: 16px;
      cursor: pointer;
      margin: 30px 0;
      display: inline-block;
    }
    .continue-btn:hover {
      background: #2980b9;
    }
  </style>
</head>
<body>

<div class="header">
  <div class="lesson-meta">Unit 1.1: Binary Trees and Binary Search Trees | Lesson 1 of 4</div>
  <h1>Binary Tree Fundamentals</h1>
</div>

<div class="intro-text">
  <strong>Binary trees</strong> are hierarchical data structures where each node has at most two children, referred to as the left child and right child. They form the foundation for advanced structures like Binary Search Trees, AVL Trees, and Heaps, making them essential for efficient searching, sorting, and data organization in real-world applications.
</div>

<h2>Core Terminology</h2>
<p>Understanding binary tree terminology is crucial for working with tree structures. Click each card to explore key concepts:</p>

<div class="flashcards">
  <div class="flashcard" style="background: #3498db;">
    <h3>Node</h3>
    <p>The basic unit containing data and references to left and right children.</p>
  </div>
  
  <div class="flashcard" style="background: #9b59b6;">
    <h3>Root</h3>
    <p>The topmost node with no parent; the entry point to the tree.</p>
  </div>
  
  <div class="flashcard" style="background: #e74c3c;">
    <h3>Leaf</h3>
    <p>A node with no children (both left and right are null).</p>
  </div>
  
  <div class="flashcard" style="background: #16a085;">
    <h3>Height</h3>
    <p>The longest path from a node to any leaf. Tree height = root height.</p>
  </div>
  
  <div class="flashcard" style="background: #f39c12;">
    <h3>Depth</h3>
    <p>The distance from the root to a node. Root has depth 0.</p>
  </div>
  
  <div class="flashcard" style="background: #34495e;">
    <h3>Subtree</h3>
    <p>A tree formed by a node and all its descendants.</p>
  </div>
</div>

<h2>Types of Binary Trees</h2>

<div class="expandable">
  <div class="expandable-header" onclick="toggleExpand(this)">
    <span><strong>Full Binary Tree</strong></span>
    <span class="arrow">▼</span>
  </div>
  <div class="expandable-content">
    <p><strong>Definition:</strong> Every node has either 0 or 2 children (no node has exactly one child).</p>
    <p><strong>Property:</strong> If there are <code>n</code> internal nodes, there are <code>n+1</code> leaves.</p>
    <p><strong>Use Case:</strong> Huffman coding trees for data compression.</p>
  </div>
</div>

<div class="expandable">
  <div class="expandable-header" onclick="toggleExpand(this)">
    <span><strong>Complete Binary Tree</strong></span>
    <span class="arrow">▼</span>
  </div>
  <div class="expandable-content">
    <p><strong>Definition:</strong> All levels are fully filled except possibly the last, which is filled from left to right.</p>
    <p><strong>Property:</strong> Height is minimized for given number of nodes: <code>⌊log₂(n)⌋</code></p>
    <p><strong>Use Case:</strong> Binary heaps in priority queues (used in Dijkstra's algorithm).</p>
  </div>
</div>

<div class="expandable">
  <div class="expandable-header" onclick="toggleExpand(this)">
    <span><strong>Perfect Binary Tree</strong></span>
    <span class="arrow">▼</span>
  </div>
  <div class="expandable-content">
    <p><strong>Definition:</strong> All internal nodes have exactly two children, and all leaves are at the same level.</p>
    <p><strong>Property:</strong> Total nodes = <code>2^(h+1) - 1</code> where h is height.</p>
    <p><strong>Use Case:</strong> Segment trees for efficient range queries.</p>
  </div>
</div>

<div class="expandable">
  <div class="expandable-header" onclick="toggleExpand(this)">
    <span><strong>Balanced Binary Tree</strong></span>
    <span class="arrow">▼</span>
  </div>
  <div class="expandable-content">
    <p><strong>Definition:</strong> Height difference between left and right subtrees is at most 1 for every node.</p>
    <p><strong>Property:</strong> Guarantees O(log n) time for search, insert, and delete operations.</p>
    <p><strong>Use Case:</strong> AVL trees and Red-Black trees in database indexing.</p>
  </div>
</div>

<h2>Basic Implementation</h2>

<div class="code-block">
<pre>
class TreeNode:
    def __init__(self, data):
        self.data = data
        self.left = None
        self.right = None

# Creating a simple binary tree
root = TreeNode(1)
root.left = TreeNode(2)
root.right = TreeNode(3)
root.left.left = TreeNode(4)
root.left.right = TreeNode(5)
</pre>
</div>

<div class="tree-visual">
Tree Structure:<br><br>
       1<br>
      / \<br>
     2   3<br>
    / \<br>
   4   5
</div>

<h2>Essential Operations</h2>

<div class="code-block">
<pre>
def height(node):
    """Calculate height of tree"""
    if node is None:
        return -1
    return 1 + max(height(node.left), height(node.right))

def count_nodes(node):
    """Count total nodes"""
    if node is None:
        return 0
    return 1 + count_nodes(node.left) + count_nodes(node.right)

def count_leaves(node):
    """Count leaf nodes"""
    if node is None:
        return 0
    if node.left is None and node.right is None:
        return 1
    return count_leaves(node.left) + count_leaves(node.right)
</pre>
</div>

<button class="continue-btn" onclick="alert('Moving to Binary Search Trees!')">CONTINUE →</button>

<script>
function toggleExpand(header) {
  const content = header.nextElementSibling;
  const arrow = header.querySelector('.arrow');
  
  content.classList.toggle('active');
  arrow.classList.toggle('rotated');
}
</script>

</body>
</html>