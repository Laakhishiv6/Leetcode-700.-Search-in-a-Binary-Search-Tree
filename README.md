# Leetcode-700.-Search-in-a-Binary-Search-Tree
# Description
You are given the root of a binary search tree (BST) and an integer val.

Find the node in the BST that the node's value equals val and return the subtree rooted with that node. If such a node does not exist, return null.
# Solution
You are given the root of a Binary Search Tree (BST) and an integer val.
Your task is to find and return the subtree rooted at the node with value val.
If the node does not exist, return null.
# Algorithm
1. Start at the root.
2. If the root is None (tree is empty), return None.
3. If root.val == val, return root (we found the node).
4. If val < root.val, recurse into the left subtree.
5. If val > root.val, recurse into the right subtree.
6. Repeat until the value is found or the search ends with None.
# Code
class Solution:

    def searchBST(self, root: Optional[TreeNode], val: int) -> Optional[TreeNode]:
        if not root:
            return None
        if root.val==val:
            return root
        elif root.val>val:
            return self.searchBST(root.left,val)
        else:
            return self.searchBST(root.right,val)
# Time Complexity
Best Case: O(1) if the root is the value.

Average/Worst Case: O(h)
where h is the height of the tree:
