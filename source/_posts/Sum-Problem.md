---
title: Sum Problem
author: Alex
avatar: https://al3xxxx.oss-cn-guangzhou.aliyuncs.com/img/20210513232724.png
authorLink: hojun.cn
authorAbout: 一个好奇的人
authorDesc: 一个好奇的人
categories: 技术
comments: true
type: index
date: 2021-03-15 22:53:38
tags:
keywords:
description:
photos: https://al3xxxx.oss-cn-guangzhou.aliyuncs.com/img/20210513222736.jpg
---
![](https://al3xxxx.oss-cn-guangzhou.aliyuncs.com/img/20210514131620.jpg)
#include <iostream>

using namespace std;

int main()
{
    int n,sum,i;
    while(cin>>n)
    {
        sum=0;
        for(i=1;i<=n;i++)
        {
            sum+=i;
        }
        cout<<sum<<endl<<endl;
    }
    return 0;
}