/*输入某二叉树的前序遍历和中序遍历的结果，请重建出该二叉树。
假设输入的前序遍历和中序遍历的结果中都不含重复的数字。
例如输入前序遍历序列{1,2,4,7,3,5,6,8}和中序遍历序列{4,7,2,1,5,3,8,6}，则重建二叉树并返回。*/

/* function TreeNode(x) {
    this.val = x;
    this.left = null;
    this.right = null;
} */
//选择前序排列的第一个数字，在中序排列中找到它的位置，也即是说，
//以这个数为根节点。中序排列在他之前的数，就是他的左子树，在他时候的数就是他的右子树。
//为了保证不越界，下一次参与递归的数组的应该以这个找到的数为界限
function reConstructBinaryTree(pre, vin)
{
    if(pre.length == 0 && vin.length == 0){
        return null;
    }//递归出口
    let i = vin.indexOf(pre[0]);
    let tree = new TreeNode(pre[0])
    tree.left = reConstructBinaryTree(pre.slice(1,i+1), vin.slice(0,i))
    tree.right = reConstructBinaryTree(pre.slice(i+1),vin.slice(i+1))
    return tree;
}
