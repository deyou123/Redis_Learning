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
 
 LRAGE key start end : 获取列表中指定范围的元素。从最右边算起
 
 
 ## Set 集合
 
 Set 是无序的，集合成员是唯一的。意味着集合中不能出现重复的数据。
 
 常用的命令： SADD、SCARD、SNENVERS、SPOP
 
 SADD key member1 member2 向集合中添加一个或多个成员
 
 SCARD key : 获取集合的成员数.
 
 SMEMBERS key : 获取集合中所有成员。
 
 SPOP key ：随机移除集合中的一个元素并返回。
 
##  Sorted Set 有序集合

 自动排序
 
 常用命令：ZADD、ZRANGE、ZREM和ZCARD.
 
 ZADD key score1 member1 添加一个或多个成员
 
 ZRANGE key start stop 获取有序集合指定区间的成员
 
 ZREM key member: 移除一个或多个成员。
 
 ZCARD key 获取有序集合的成员数。



ZADD key score1 member1 [score2 member2]
向有序集合添加一个或多个成员，或者更新已存在成员的分数




ZCARD key
获取有序集合的成员数




ZCOUNT key min max
计算在有序集合中指定区间分数的成员数




ZINCRBY key increment member
有序集合中对指定成员的分数加上增量 increment




ZINTERSTORE destination numkeys key [key ...]
计算给定的一个或多个有序集的交集并将结果集存储在新的有序集合 key 




ZLEXCOUNT key min max
在有序集合中计算指定字典区间内成员数量




ZRANGE key start stop [WITHSCORES]
通过索引区间返回有序集合成指定区间内的成员




ZRANGEBYLEX key min max [LIMIT offset count]
通过字典区间返回有序集合的成员




ZRANGEBYSCORE key min max [WITHSCORES] [LIMIT]
通过分数返回有序集合指定区间内的成员




ZRANK key member
返回有序集合中指定成员的索引




ZREM key member [member ...]
移除有序集合中的一个或多个成员




ZREMRANGEBYLEX key min max
移除有序集合中给定的字典区间的所有成员





ZREMRANGEBYRANK key start stop
移除有序集合中给定的排名区间的所有成员




ZREMRANGEBYSCORE key min max
移除有序集合中给定的分数区间的所有成员




ZREVRANGE key start stop [WITHSCORES]
返回有序集中指定区间内的成员，通过索引，分数从高到底




ZREVRANGEBYSCORE key max min [WITHSCORES]
返回有序集中指定分数区间内的成员，分数从高到低排序





ZREVRANK key member
返回有序集合中指定成员的排名，有序集成员按分数值递减(从大到小)排序




ZSCORE key member
返回有序集中，成员的分数值



ZUNIONSTORE destination numkeys key [key ...]
计算给定的一个或多个有序集的并集，并存储在新的 key 中



ZSCAN key cursor [MATCH pattern] [COUNT count]
迭代有序集合中的元素（包括元素成员和元素分值）


