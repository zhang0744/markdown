# mysql



mysql教程:<http://c.biancheng.net/mysql/>



select查询完整语句
```sql
SELECT [聚合函数] 字段名 as 别名, select_expr [,select_expr,…] [
FROM tb_name/*表名*/
[JOIN 表名]
[ON 连接条件]
[WHERE 条件判断]
[GROUP BY {col_name | postion} [ASC | DESC], …]
[HAVING WHERE 条件判断]
[ORDER BY {col_name|expr|postion} [ASC | DESC], …]
[ LIMIT {[offset,]rowcount | row_count OFFSET offset}]
]

```

  以上每个步骤都会产生一个虚拟表，该虚拟表被用作下一个步骤的输入。这些虚拟表对调用者(客户端应用程序或者外部查询)不可用。只有最后一步生成的表才会会给调用者。如果没有在查询中指定某一个子句，将跳过相应的步骤。

逻辑查询处理阶段简介：
1、 FROM：对 FROM 子句中的前两个表执行笛卡尔积(交叉联接)，生成虚拟表 VT1。
2、 ON：对 VT1 应用 ON 筛选器，只有那些使为真才被插入到 TV2。
3、 OUTER (JOIN):如果指定了 OUTER JOIN(相对于 CROSS JOIN 或 INNER JOIN)，保留表中未找到匹配的行将作为外部行添加到 VT2，生成 TV3。如果 FROM子句包含两个以上的表，则对上一个联接生成的结果表和下一个表重复执行步骤 1 到步骤 3，直到处理完所有的表位置。
4、 WHERE：对 TV3 应用 WHERE 筛选器，只有使为 true 的行才插入 TV4。
5、 GROUP BY：按 GROUP BY 子句中的列列表对 TV4 中的行进行分组，生成 TV5。
6、 CUTE|ROLLUP：把超组插入 VT5，生成 VT6。
7、 HAVING：对 VT6 应用 HAVING 筛选器，只有使为 true 的组插入到 VT7。
8、 SELECT：处理 SELECT 列表，产生 VT8。
9、 DISTINCT：将重复的行从 VT8 中删除，产品 VT9。
10、 ORDER BY：将 VT9 中的行按 ORDER BY 子句中的列列表顺序，生成一个游标(VC10)。
11、 TOP：从 VC10 的开始处选择指定数量或比例的行，生成表 TV11，并返回给调用者。
————————————————
原文链接：https://blog.csdn.net/m19123456789/article/details/83795665









数据库存金额数据字段类型 : `decimal`