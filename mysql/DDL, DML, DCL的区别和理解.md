# DDL, DML, DCL的区别和理解

- SQL语言共分为4大类: DQL(数据查询语言), DML(数据操纵语言), DDL(数据定义语言), DCL(数据控制语言)

1. DQL(数据查询语言)

- 数据查询语言的基本结构是 SELECT 子句, FROM 子句, WHERE 子句组成的查询块

```
SELECT <字段名>
FROM <表或视图名>
WHERE <查询条件>
```

2. DML(数据操纵语言)

- INSERT(插入)

- UPDATE(更新)

- DELETE(删除, 可以回滚)

3. DDL(数据定义语言)

- CREATE(创建)

- ALTER(修改表结构)

- RENAME(修改表名或列名)

- DROP(删除表中的数据或结构, 不能回滚)

- TRUNCATE(删除表中的数据, 不删除表结构, 不能回滚, 比DELETE效率高)

4. DCL(数据控制语言)

- GRANT(授权)

- REVOKE(回收权限)

## 扩展

- TCL(事务控制语言)

- SAVEPOINT(保存点)

- ROLLBACK(回退到某点)

- COMMIT(提交事务)
