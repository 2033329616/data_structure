<head>
    <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
    <script type="text/x-mathjax-config">
        MathJax.Hub.Config({
            tex2jax: {
            skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
            inlineMath: [['$','$']]
            }
        });
    </script>
</head>


# 数据库

[TOC]
## 1. 数据库基本概念
>主键 (PRIMARY KEY)：主键是能确定一条记录的唯一标识，不为空

比如，一条记录包括身份正号、姓名、年龄，身份证号是唯一能确定你这个人的，其他都可能有重复，所以身份证号是主键
>外键：用于与另一张表的关联

能确定另一张表记录的字段，用于保持数据的一致性。比如，A表中的一个字段，是B表的主键，那它就是A表的外键

>唯一约束 (UNIQUE)：该属性的值也不能重复，但可以为NULL

## 2. 数据库性质
- 任意两行的主键值不相同
- 主键列不允许NULL值
- 表可包含多个唯一约束，但每个表只允许**一个主键**
- 唯一约束列可以为NULL值，但每个NULL值都是唯一的 ($\text{NULL} \neq \text{NULL}$)