- 👋 Hi, I’m @Kratika28-agr
- 🌱 I’m currently learning CP
- 📫 How to reach me kratikaagrawal8@gmail.com
#144-BinaryTreePreorderTraversal solution LeetCode 
class Solution {
    public List<Integer> preorderTraversal(TreeNode root) {
        List<Integer> ans=new ArrayList<>();
        if (root == null)
            return ans;
        
        Stack<TreeNode> s= new Stack<>();
        s.push(root);
        
        while(!s.isEmpty()){
            TreeNode temp=s.pop();
            ans.add(temp.val);
            if(temp.right!=null)
                s.push(temp.right);
             if(temp.left!=null)
                s.push(temp.left);
        }
        return ans;
    }
}
