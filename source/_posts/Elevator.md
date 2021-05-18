---
title: Elevator
author: Alex
avatar: https://al3xxxx.oss-cn-guangzhou.aliyuncs.com/img/20210513232724.png
authorLink: hojun.cn
authorAbout: 一个好奇的人
authorDesc: 一个好奇的人
categories: 技术
comments: true
type: index
date: 2021-03-28 20:02:50
tags: HDU
keywords:
description: HDU1008
photos: https://al3xxxx.oss-cn-guangzhou.aliyuncs.com/img/20210513222736.jpg
---
![](https://al3xxxx.oss-cn-guangzhou.aliyuncs.com/img/20210514135211.jpg)
```js
int main()
{
    int n,i,a[100],time,stop;
    while(scanf("%d",&n)!=EOF)
    {
        time=0;
        stop=0;
        if(n==0)
            break;
        time = 0;
        for(i=0;i<n;i++)
        {
            scanf("%d",&a[i]);
        }

        for(i=0;i<n;i++)
        {
            if(a[i]>stop)
            {
                time += (a[i]-stop)*6;
                time+=5;
            }
            else
            {
                time += (stop-a[i])*4;
                time+=5;
            }
            stop=a[i];
        }
        printf("%d\n",time);
    }
    return 0;
}
```