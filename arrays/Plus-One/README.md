# [66. Plus One](https://leetcode.com/problems/plus-one)

## Description

<p>Given a <strong>non-empty</strong> array of decimal digits&nbsp;representing a non-negative integer, increment&nbsp;one to the integer.</p>

<p>The digits are stored such that the most significant digit is at the head of the list, and each element in the array contains a single digit.</p>

<p>You may assume the integer does not contain any leading zero, except the number 0 itself.</p>

<p>&nbsp;</p>
<p><strong>Example 1:</strong></p>

<pre>
<strong>Input:</strong> digits = [1,2,3]
<strong>Output:</strong> [1,2,4]
<strong>Explanation:</strong> The array represents the integer 123.
</pre>

<p><strong>Example 2:</strong></p>

<pre>
<strong>Input:</strong> digits = [4,3,2,1]
<strong>Output:</strong> [4,3,2,2]
<strong>Explanation:</strong> The array represents the integer 4321.
</pre>

<p><strong>Example 3:</strong></p>

<pre>
<strong>Input:</strong> digits = [0]
<strong>Output:</strong> [1]
</pre>

<p>&nbsp;</p>
<p><strong>Constraints:</strong></p>

<ul>
	<li><code>1 &lt;= digits.length &lt;= 100</code></li>
	<li><code>0 &lt;= digits[i] &lt;= 9</code></li>
</ul>

## Solutions

<!-- tabs:start -->

### **Java**

```java
class Solution {
    public int[] plusOne(int[] digits) {
        int n = digits.length;
        for (int i = n - 1; i >= 0; --i) {
            ++digits[i];
            digits[i] %= 10;
            if (digits[i] != 0) {
                return digits;
            }
        }
        digits = new int[n + 1];
        digits[0] = 1;
        return digits;
    }
}
```

<!-- tabs:end -->