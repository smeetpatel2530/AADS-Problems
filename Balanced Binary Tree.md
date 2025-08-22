# Balanced Binary Tree


```cpp
class Solution {

public:
    bool isBalanced(TreeNode* root) {
        return dfs_height(root) != -1;
    }
    int dfs_height(TreeNode* root) {
        if (root == NULL) return 0;
        int leftHeight = dfs_height(root->left);
        if (leftHeight == -1) 
            return -1;
        int rightHeight = dfs_height(root->right);
        if (rightHeight == -1) 
            return -1;
        if (abs(leftHeight - rightHeight) > 1)  
            return -1;
        return max(leftHeight, rightHeight) + 1;
    }
};

```

## Time Complexity = O(N)
## Space Complexity = O(N)

