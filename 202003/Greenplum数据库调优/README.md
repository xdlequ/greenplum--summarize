# Greenplum 数据库调优
	以下主要是《Greenplum 数据库调优》的目录，
	详细的文档请查看:https://github.com/xfg0218/greenplum--summarize/tree/master/greenplum%E5%AD%A6%E4%B9%A0pdf%E6%96%87%E6%A1%A3/Greenplum%E4%BB%8E%E5%85%A5%E9%97%A8%E5%88%B0%E7%B2%BE%E9%80%9A
# 1 Greenplum查询处理回顾
	1.1 Master 把查询语句分发到segment
# 2 Greenplum数据库调优
	2.1 系统资源
	2.2 硬件问题
	2.3 资源管理
		2.3.1 查看resource queue的参数
		2.3.2 设置临时的内存大小
		2.3.3 当发生数据溢出时添加内存的大小
		2.3.4 受影响的系统的参数
		2.3.5 查看一些有用的视图
	2.4 统计信息不准确
		2.4.1 创建两张表
		2.4.2 使用EXPLAIN查看执行计划
		2.4.3 使用ANALYZE执行统计信息
		2.4.4 以下情况都需要执行ANALYZE
	2.5 数据倾斜
		2.5.1 数据倾斜实例
		2.5.2 使用视图查看表的倾斜
		2.5.3 改变数据倾斜问题
	2.6 计算倾斜
		2.6.1 关联条件倾斜
		2.6.2 多计算聚集
		2.6.3 减少计算倾斜问题
	2.7 数据广播
		2.7.1 查看表是不是出现了Broadcast
		2.7.2 改变planner之后运行
		2.7.3 修改GUC来设定优化器
	2.8 多阶段聚集
		2.8.1 多阶段聚集关闭的情况
		2.8.2 多阶段聚集打开的情况
		2.8.3 GUC会影响优化器对多阶段聚集的选择
	2.9 分区裁剪
		2.9.1 定义分区
		2.9.2 使用查询计划查看分区
		2.9.2.1 planner 分区
		2.9.2.2 ORCA分区
		2.9.2.3 最优查询条件
# 3 一些最佳实战
	3.1 最佳实践注意点