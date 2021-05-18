---
title: A + B Problem Ⅱ
author: Alex
avatar: https://al3xxxx.oss-cn-guangzhou.aliyuncs.com/img/20210513232724.png
authorLink: hojun.cn
authorAbout: 一个好奇的人
authorDesc: 一个好奇的人
categories: 技术
comments: true
type: index
date: 2021-03-16 00:44:43
tags: HDU
keywords:
description: HDU1002
photos: https://al3xxxx.oss-cn-guangzhou.aliyuncs.com/img/20210513222736.jpg
---
![](https://al3xxxx.oss-cn-guangzhou.aliyuncs.com/img/20210514135211.jpg)
```js
#include<stdio.h>
#include<stdlib.h>
#include<string.h>
int main()
{
    char st1[1001],st2[1001];
    int T,i,a[1001],b[1001],len1,len2,j;
    scanf("%d",&T);
        j=0;
        while(T--)
        {
            j++;
            memset(a,0,sizeof(a));
            memset(b,0,sizeof(b));
            scanf("%s",st1);
            len1=strlen(st1);
            for(i=1;i<=len1;++i)
            {
                a[i]=st1[len1-i]-48;
            }
            scanf("%s",st2);
            len2=strlen(st2);
            for(i=1;i<=len2;++i)
            {
                b[i]=st2[len2-i]-48;
            }
            if(len1<len2)
                len1=len2;
            for(i=1;i<=len1;i++)
            {
                a[i]+=b[i];
                a[i+1]+=a[i]/10;
                a[i]%=10;
            }
            if(a[len1+1]>0)
                len1++;
                printf("Case %d:\n%s + %s = ",j,st1,st2);
            for(i=len1;i>=1;--i)
            {
                printf("%d",a[i]);
            }
            if(T!=0)
            printf("\n\n");
            else
                printf("\n");
        }
    return 0;
}
```