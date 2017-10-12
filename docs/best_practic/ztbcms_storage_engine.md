## ZtbCMS数据库的存储引擎

ZtbCMS所有表的存储引擎(包括创建模型)默认是: InnoDB [从v3.2.0.0]

考虑到大部分情况下：

1. 对事务需要不高，除了支付，余额统计，收益记录等
2. 查询远大于插入
3. MyISAM 本身支持FULLTEXT索引，InnoDB直到My SQL 5.6.4才支持

若需要事务需求，请自行对该表的存储引擎改为 InnoDB


### 阅读参考

[MySQL 5.5手册 - 存储引擎介绍](http://dev.mysql.com/doc/refman/5.5/en/storage-engines.html)



