---
layout:         post
title:          Single Number
description:    求单个数
keywords: array, XOR
---
## Single Number

### 原题列表
> Given an array of integers, 
> every element appears twice except for one.
> Find that single one.

#### **Note:**
> Your algorithm should have a linear runtime complexity. 
> Could you implement it without using extra memory?
   
### 分析 

> 采用异或的方法，即相同的数异或为0，不相同的数异或为1.
> 公式如下: a ⊕ b ⊕ a = b.异或的自反性.
 
### 代码

<pre name="colorcode" class="js">
class Solution {
public:
 int singleNumber(int A[], int n) {
        int x=0;
        for(size_t i=0;i<n;i++)
            x^=A[i];
        return x;
  }
};
</pre>

来源： <https://leetcode.com/problems/single-number/>