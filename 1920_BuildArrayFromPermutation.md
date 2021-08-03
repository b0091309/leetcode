时间：2021/08/03
Given a zero-based permutation nums (0-indexed), build an array ans of the same length where ans[i] = nums[nums[i]] for each 0 <= i < nums.length and return it.
A zero-based permutation nums is an array of distinct integers from 0 to nums.length - 1 (inclusive).
给定一个从0开始的阵列，回传一个名为ans的阵列，
条件为ans[i] = nums[nums[i]]

Follow-up: Can you solve it without using an extra space (i.e., O(1) memory)?
进阶：空间复杂度要求，是否能在不使用额外空间下完成

解题结果：
普通：完成
进阶：失败

进阶：
思路1，暴力解法（无效)
原因：因为置换num[0]的当下，整个列表就乱了
public int[] buildArray(int[] nums) {
    for(int i = 0; i < nums.length; i++){
        nums[i] = nums[nums[i]];
    }
    return nums;
}
思路2，递归（没写出来）

官方解：
题解：
解法1：1000进位法
https://leetcode-cn.com/problems/build-array-from-permutation/solution/ji-yu-pai-lie-gou-jian-shu-zu-by-leetcod-gjcn/
OS 说不能有新空间，但没说不能利用array的其他空间...
解法2：10进制搭配左右移>><<(尚无法理解)
https://leetcode.com/problems/build-array-from-permutation/discuss/1315480/Java-or-O(1)-Space-O(n)-Time
