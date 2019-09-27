# 7种数据类型

## 1. String 字符串类型 ， key 没啥可说的，value 的五种数据类型字符串、数字、二进制、和Json 数据类型。

key 的设置区分大小写。
get set del 三种简单命令
incr key :就是key 自增1，不存在自增后get(key)=1
DECR key :就是key 自减1，不存在则返回k
append key value 将value 追加到旧的value上。
STRLEN key 返回字符串长度
INCRBYFLOAT key 3.5 在value上追加对应的值为3.5
GETRANGE key start end 获取指定字符串下标的所有值。

## Hash 哈希

 用来存储对象，value实际上就是一个map,里面所有的属性都可以单独修改新增删除。常用命令HGET、 HSET、HGETALL.
 HGET key field 获取key 指定字段的值
 HSET key field value  设置key指定字段的值
 HGETALL key 获取在哈希表中指定key 的所有字段和值
 
 ## List 列表
 
 一种简单的字符串集合，有序的。是链表结构。在实际中可以轻松实心消息排行等功能。
 常用命令：LPUSH、 RPUSH、LPOP、RPOP、和LRANGE.
 LPUSH key value1 [value2] : 在列表头部添加一个或多个值。
 RPUSH key value1 [value2] : 在列表尾部添加一个或多个值。
 LPOP key 移除列表中第一个元素。
 RPOP key 移除列表中最后一个元素。
 LRAGE key start end : 获取列表中指定范围的元素。从最右边算起，
 
