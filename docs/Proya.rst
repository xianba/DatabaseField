============
Proya数据库
============

Proya项目是一个业务复杂，多类型数据库的海量数据维护、管理和分析项目，其中涉及到CRM、SRM、企业OA等关联数据库。这个项目主要是根据相关数据库整理的字段管理表，方便数据库设计、开发以及后续报表实现。



数据库表
=========

+------------------------+------------------------+------------------------+
| 数据库表名             | 中文描述               | 相关业务               |
+========================+========================+========================+
| Account                | 经销商信息表           | 记录经销商信息的表     |
+------------------------+------------------------+------------------------+
| Order                  | 订单信息表             | 记录经销商所下订单表   |
+------------------------+------------------------+------------------------+
| OrderDetail            | 订单明细信息表         | 每个订单所包含的明细   |
+------------------------+------------------------+------------------------+

Account
========

+------------------------+------------------------+------------------------+------------------------+------------------------+
| 字段                   | 字段类型               | 中文描述               | 限制条件               | 关联表字段             |
+========================+========================+========================+========================+========================+
| Id                     | UUID                   | 经销商主键序号         | 无重复项               |                        |
+------------------------+------------------------+------------------------+------------------------+------------------------+
| Number                 | 整型                   | 经销商编码（8位）      | 系统内唯一             | Channel.AccountNo      |
+------------------------+------------------------+------------------------+------------------------+------------------------+
| Name                   | 字符型                 | 经销商名称             |                        | Order.AccountName      |
+------------------------+------------------------+------------------------+------------------------+------------------------+
| Address                | 字符型                 | 经销商地址             |                        |                        |
+------------------------+------------------------+------------------------+------------------------+------------------------+

