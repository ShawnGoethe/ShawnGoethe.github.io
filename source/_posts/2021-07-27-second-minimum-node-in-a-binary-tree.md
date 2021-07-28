---
title: 2021-07-27-second-minimum-node-in-a-binary-tree
date: 2021-07-27 21:53:51
tags:
- Easy
categories:
- LeetCode 
---

# Leetcode 671

#### [671. 二叉树中第二小的节点](https://leetcode-cn.com/problems/second-minimum-node-in-a-binary-tree/)

难度简单198收藏分享切换为英文接收动态反馈

给定一个非空特殊的二叉树，每个节点都是正数，并且每个节点的子节点数量只能为 `2` 或 `0`。如果一个节点有两个子节点的话，那么该节点的值等于两个子节点中较小的一个。

更正式地说，`root.val = min(root.left.val, root.right.val)` 总成立。

给出这样的一个二叉树，你需要输出所有节点中的**第二小的值。**如果第二小的值不存在的话，输出 -1 **。**

 

**示例 1：**

![img](https://assets.leetcode.com/uploads/2020/10/15/smbt1.jpg)

```
输入：root = [2,2,5,null,null,5,7]
输出：5
解释：最小的值是 2 ，第二小的值是 5 。
```

**示例 2：**

![img](https://assets.leetcode.com/uploads/2020/10/15/smbt2.jpg)

```
输入：root = [2,2,2]
输出：-1
解释：最小的值是 2, 但是不存在第二小的值。
```

 

**提示：**

- 树中节点数目在范围 `[1, 25]` 内
- `1 <= Node.val <= 231 - 1`
- 对于树中每个节点 `root.val == min(root.left.val, root.right.val)`

# Solution

如题意，父节点就是最小值，借鉴了答案，递归条件写错了

```js
/**
 * Definition for a binary tree node.
 * function TreeNode(val, left, right) {
 *     this.val = (val===undefined ? 0 : val)
 *     this.left = (left===undefined ? null : left)
 *     this.right = (right===undefined ? null : right)
 * }
 */
/**
 * @param {TreeNode} root
 * @return {number}
 */
var findSecondMinimumValue = function (root) {

    let ans = -1;
    const parentValue = root.val;//root value

    const dfs = (node) => {
        if (node === null) {
            return;
        }
        if (ans !== -1 && node.val >= ans) {
            return;
        }
        if (node.val > parentValue) {
            ans = node.val;
        }
        dfs(node.left);
        dfs(node.right);
    }

    dfs(root);
    return ans;
};
```

