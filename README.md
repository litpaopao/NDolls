NDolls
======

ORM Framework
实体类字段分为两种类型：数据字段、关联对象字段
1.数据库数据字段名应与Model实体类保持一致；
2.两表之间的主外键名称应一致；
3.Attribute类在使用时Attribute可省略不写，如[AssociationAttribute]等效于[Association]

2014.4.11
1.已完成级联添加、级联修改、级联查询（还差级联删除）；
2.EntityUtil的Persist方法对调用DBTransaction未来还需改进以支持多数据库；
3.RepositoryFactory类的CreateRepository未来还需改进以支持多数据库；
4.Repository仍可再进一步抽象出RepositoryBase基类，存储泛型T的表名和主键信息；
5.分页查询还未涉及；

2014-9-15
1.支持自动编号数据库字段

2014.4.12
1.完成基于Model配置的自动验证功能。

2014.4.13
1.改进Model自动验证正则配置方式功能，Model中Validate特性即可使用框架内置好的匹配验证模式，也可使用自定义的正则模式。

2014.5.2
1.修改按自定义条件查询方法，支持不等于条件项（ConditionItem）

2014.7.14
1.增加分页支持（但页数展示还未支持）；
2.增加联合主键支持（但关联对象还不支持联合主键）；
3.修改按自定义条件查询方法，支持子集查询条件项（ValuesIn）

2014.9.15
1.增加自动编号支持

2014.10.14
1.调整sql语句生成代码结构，更清晰；
2.丰富按条件删除功能；
3.增加用户非查询sql直接执行；
4.增加用户自写条件sql查询功能；

2014.11.12
1.优化多条件查询，修复同一字段多次作为条件传入出错问题；

2014.11.18
1.添加ValuesNotIn（不包含）查询支持
2.添加exist按ConditionItem条件查询支持

2014.11.20
1.增加ModelAttribute配置支持多validate检测
2.支持Model的ValidateAttribute配置用户自定义提示

2014.11.21
1.增加查询排序支持

2014.12.24
1.增加Model用户自定义Attribute支持；