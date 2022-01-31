/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode() : val(0), left(nullptr), right(nullptr) {}
 *     TreeNode(int x) : val(x), left(nullptr), right(nullptr) {}
 *     TreeNode(int x, TreeNode *left, TreeNode *right) : val(x), left(left), right(right) {}
 * };
 */
class Solution {
public:
    vector<string> ans;
    void FindPath(TreeNode* root, string path)
    {
        if(root==NULL)
            return;
        if(root->left==NULL && root->right==NULL)
        {
            path+=to_string(root->val);
            ans.push_back(path);
            return;
        }
        path+=to_string(root->val)+"->";
        FindPath(root->left, path);
        FindPath(root->right, path);
    }
    vector<string> binaryTreePaths(TreeNode* root) {
        string s="";
        FindPath(root,s);
        return ans;
    }
};
