# 数据收集层

### 关系型数据的收集

#### 1. Sqoop（SQL on Hadoop）  
采用MapReduce进行全量关系型数据的收集。  
桥梁作用：  
![Sqoop的"桥梁"作用](../img/img02.png)
Sqoop2基本架构：  
![Sqoop2基本结构](../img/img03.png)

如何高效地增量收集数据？CDC（Change Data Capture）！  

#### 2. Canal（阿里）Databus（LinkedIn）
Canal基本原理与架构  
![Canal基本原理、基本架构](../img/img04.png)

为了解决多机房数据同步问题，Otter，基于Canal。  

#### 3. Otter
基本架构  
![Otter基本架构](../img/img05.png)

#### 非关系型数据的收集

日志收集挑战：  
> 数据源种类繁多  
> 数据源是物理分布的  
> 流式的，不间断产生  
> 对可靠性有一定要求  

#### 1. Flume
特点：  
> 良好的扩展性  
> 高度定制化  
> 声明式动态化配置  
> 语义路由  
> 良好的可靠性  

Flume NG（OG已经废弃）基本架构  
![Flume基本构成](../img/img06.png)
Flume Agent基本构成  
![Flume Agent基本构成](../img/img07.png)
Flume NG高级组件  
![Flume Agent内部高级组件](../img/img08.png)

