# 第一次深入学习

## Redis数据结构

我将阐述redis数据库的几种数据类型，
String：最基础的键值对，不同于java的String，redis的String能存储数字和字符串等。
Hash:Hash是一个key可以对应多个元素，因为String如果要存储对象的话使用json，不方便修改对象某属性，对Hash的操作要指定具体
的field。
Set：与java中的HashSet相似，相当于一个Key下面有多个元素，元素不能重复，无序。支持交集、并集、差集运算（SINTER/SUNION/SDIFF），这是实际使用中非常高频的功能，比如共同好友、标签匹配等场景。
List:相当于java的双向链表，可以从两侧插入和pop数据，这种结构也许可以用于队列的设计。除了队列，也可以当栈用（同一端 push + pop）

## Key层级结构

Key的层级结构：redis里的key可以设置多层结构，就像文件夹的目录一样，使用：分割层级