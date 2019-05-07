# Presto - 0.107/0.205

## Presto是Facebook开源的，基于内存的分布式SQL查询引擎。

## 概述

##### Presto支持在线数据查询，包括Hive(HDFS), Cassandra, 关系数据库(Oracle/MYSQL)以及专有数据存储(**Kafka**)。一条Presto查询可以将多个数据源的数据进行合并，可以跨越整个组织进行分析。
##### Presto是专门为大数据实时查询计算而设计而开发的产品。基于Java语言开发。
##### Presto被设计为数据仓库和数据分析产品：数据分析、大规模数据聚集和生成报表。这些工作经常通常被认为是线上分析处理操作。
##### Presto硬件集群必须满足大内存、万兆网络和高计算能力的特点。

#### 节点类型
| Coordinator(单独的节点)                                 | Worker(多个节点)  |
|-------------------------------------------------------|---------|
| 接收查询请求、解析查询语句、生成查询执行计划、任务调度和Worker管理| 执行被分解后的查询执行任务：Task |

#### DataSource
##### 在$PRESTO_HOME/etc/catalog下ali.taobao.market.properties配置文件，设置属性connector.name定义数据源的驱动器，如Hive-cdh5。
##### 命名规则：catalog.schema.table.properties ,内容connector.name=Hive-cdh5
 
|   Connector  | Catalog  | Schema   |  Table |
|-------------|---------|---------|-------|
|  数据源的驱动器 | 数据库实例 | Database | Table |

##### Hadoop的计算框架Map-Reduce，支持大数据的离线和批量计算。强调的是吞吐量而不是计算效率。Hadoop-CDH
##### Hive 数据源Hive-CDH5 or Hive-CDH4

## Presto RestFul 接口

### presto-main 工程

#### Statement 接口
StatementResource

#### Query 接口
QueryResource

#### State 接口
StateResource

#### Task 接口
TaskResource



LTS 分布式调度


https://github.com/prestodb/presto