# [88. Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array)

## Description

<p>Given two sorted integer arrays <code>nums1</code> and <code>nums2</code>, merge <code>nums2</code> into <code>nums1</code> as one sorted array.</p>

<p>The number of elements initialized in <code>nums1</code> and <code>nums2</code> are <code>m</code> and <code>n</code> respectively. You may assume that <code>nums1</code> has a size equal to <code>m + n</code> such that it has enough space to hold additional elements from <code>nums2</code>.</p>

<p>&nbsp;</p>
<p><strong>Example 1:</strong></p>
<pre><strong>Input:</strong> nums1 = [1,2,3,0,0,0], m = 3, nums2 = [2,5,6], n = 3
<strong>Output:</strong> [1,2,2,3,5,6]
</pre><p><strong>Example 2:</strong></p>
<pre><strong>Input:</strong> nums1 = [1], m = 1, nums2 = [], n = 0
<strong>Output:</strong> [1]
</pre>
<p>&nbsp;</p>
<p><strong>Constraints:</strong></p>

<ul>
	<li><code>nums1.length == m + n</code></li>
	<li><code>nums2.length == n</code></li>
	<li><code>0 &lt;= m, n &lt;= 200</code></li>
	<li><code>1 &lt;= m + n &lt;= 200</code></li>
	<li><code>-10<sup>9</sup> &lt;= nums1[i], nums2[i] &lt;= 10<sup>9</sup></code></li>
</ul>

## Solutions

<!-- tabs:start -->

### **Java**

```java
class Solution {
    public void merge(int[] nums1, int m, int[] nums2, int n) {
        int i = m - 1, j = n - 1, k = m + n - 1;
        while (j >= 0) {
            if (i >= 0 && nums1[i] > nums2[j]) {
                nums1[k--] = nums1[i--];
            } else {
                nums1[k--] = nums2[j--];
            }
        }
    }
}
```

<!-- tabs:end -->