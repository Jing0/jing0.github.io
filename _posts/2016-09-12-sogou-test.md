---
layout: post
title: "2016搜狗校园招聘笔试（Java 岗位）编程题题解"
description: 2016搜狗校园招聘笔试编程题题解
keywords: 校园招聘,笔试,题解,Java
category: code
tagline: "--read & think"
tags: [校园招聘,笔试, 题解, Java]
published: false
---

* 岗位：Java 开发
* 笔试时间：09/12/2016

# 第一题 距离的总和

### 题目描述：
 
定义两个大于2的偶数之间的距离，为这两个数之间质数的个数。从小到大输入n个大于2的偶数，输出所有数两两之间距离的总和（应该有n*(n-1)/2个距离，输出总和就好)。
	
### 输入

第一行是输入偶数的个数，最小为2，最大可能到几万。之后每行为一个偶数，最小是4，最大可能是几百万，不重复的升序排列。

### 输出

输出数据两两间距离的总和，这应该是一个不小于0的整数。

样例输入
	
	3
	4
	6
	12

样例输出

	6
	

开始我使用二重循环算出结果，即下面的代码（vec 存储的是相邻两个数之间的距离）

    for (long i = 0; i < n - 1; ++i) {
        long tmp = 0;
        for (long j = i; j < n - 1; ++j) {
            tmp += vec.at(i);
            sum += tmp;
        }
    }

但这样是会超时的。

题目中说给的顺序是升序的，这样就可以去掉二重循环。先算出第一个数到剩余所有数的距离之和，然后减去 n - 1 个第一个数到第二个数的距离，就是第二个数到剩余所有数的距离之和。

C++ 代码如下：

    #include <stdio.h>
    #include <vector>
    #define MAXN 10000010
    using namespace std;
    
    // notPrime 数组：1 为合数，0为质数
    int notPrime[MAXN] = {0};
    int main() {
        /* 下标筛选法求质数数组 */
        notPrime[0] = 1;
        notPrime[1] = 1;
        for (long i = 2; i < MAXN; ++i) {
            if (!notPrime[i]) {
                for (long j = 2; i * j < MAXN; ++j) {
                    notPrime[i * j] = 1;
                }
            }
        }
        
        long n;
        scanf("%ld", &n);
        /* 求出相邻两个数之间的距离，即之间质数的个数。用 vector 保存 */
        long num, lastnum;
        scanf("%ld", &num);
        vector<long> vec;
        for (long i = 1; i < n; ++i) {
            lastnum = num;
            scanf("%ld", &num);
            long count = 0;
            for (long j = lastnum + 1; j < num; j += 2) {
                if (!notPrime[j]) {
                    count++;
                }
            }
            vec.push_back(count);
        }
        
        /* 求出结果。
         * 本可以使用二重循环求出，但那样是会超时的。
         * 这里先求出第一个数到剩余所有数的距离之和，
         * 然后将求出的和减去第一个数到第二个数的距离乘以 n - 1 即为第二个数到后面所有数的距离。
         * 按此思想即可算出结果 */
        long sum = 0;
        long tmp = 0;
        for (long i = 0; i < n - 1; ++i) {
            tmp += vec.at(i);
            sum += tmp;
        }
        tmp = sum;
        for (long i = 1; i < n - 1; ++i) {
            tmp -= vec.at(i - 1) * (n - i);
            sum += tmp;
        }
        printf("%ld\n", sum);
        return 0;
    }


# 第二题 一个字符串的最大回文前缀长度

### 题目描述：

求一个字符串的最大回文前缀长度。回文是指正反方向读起来都一样的字符串，比如“abcdcba”就是一个回文。

### 输入

一个文本文件，至少包含一个字节。每个字节是一个字符。最大长度可能有几十万字节。

### 输出

最大回文前缀的长度。

样例输入

	sogou

样例输出

	1


直接求解即可。最开始按完整字符串算，即从第一个字符到最后一个字符；接着从第一个字符到倒数第二个字符……如果是回文，直接输出，然后退出，这样一定是最长的。

C 代码如下：

    #include <stdio.h>
    #include <string.h>
    #define MAXN 1000000
    
    char str[MAXN];
    int main() {
        scanf("%s", str);
        long i = strlen(str) - 1;
        long ans = 0;
        for (i = len - 1; i >= 0; --i) {
            long j = i;
            long count = 0;
            while (count <= j - count && str[count] == str[j - count]) {
                count++;
            }
            if (count > j - count) {
                printf("%ld\n", j + 1);
                break;
            }
        }
        return 0;
    }



只是感觉搜狗的笔试好简单，而且不严格。编程题可以随意切出不说，而且选择题提交后还可以反复修改……当然，我没有去钻这个空子。还有四十分钟时，就交卷了。