---
layout:         post
title:          Best Profit
description:    求最大收益
keywords: vector Greedy
---
##问题
>   Say you have an array for which the ith element is the price of a given stock on day .

> Design an algorithm to find the maximum profit. You may complete as many transactions as you like (ie, buy one and sell one share of the stock multiple times). However, you may not engage in multiple transactions at the same time (ie, you must sell the stock before you buy again).

> Tags: Array Greedy

>来源： <https://leetcode.com/problems/best-time-to-buy-and-sell-stock-ii/>

###分析
> 股票买法，低买高卖，把所有正价的差价加起来。

###代码
{% highlight C %}
class Solution {
public:
    int maxProfit(vector<int> &prices) {
       int sumProfit=0;
       for(int i=1;i<prices.size();++i)
       {
           if(prices[i]>prices[i-1])
           {
               sumProfit=sumProfit+prices[i]-prices[i-1];
           }
       }
        return sumProfit;  
    }
}; 
{% endhighlight %}
