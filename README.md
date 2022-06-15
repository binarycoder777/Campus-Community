# 校园E社区
描述：亦在为在校大学生提供分享、交流校园趣事而搭建的校园交流平台，实现了发帖、评论、私信、通知、 搜索、权限、统计等功能。
技术栈:SpringBoot/Kafka/Redis/Elasticsearch/Quartz/Caffine  
技术方案:
- 使用 SpringSecrity 进行认证授权，实现了多重角色、URL 级别的权限管理，增强系统安全性。 
- 使用 Caffeine+Redis 实现两级缓存，对热门帖子进行优化，提升查询效率，减轻数据库压力。 
- 使用 Kafka 对站内消息通知进行异步处理，Redis 实现点赞关注功能，从而提升系统吞吐量。 
- 使用 Elasticsearch 实现全文检索，提高检索帖子效率，并提供高亮显示和搜索词补全，优化用户体验。 
- 使用 Quartz 实现了任务调度功能，并实现了定时计算帖子分数、更新热门帖子等，对系统热门进行优化。 
- 使用 HyperLogLog、Bitmap 分别实现了 UV、DAU 的统计功能，100 万用户数据不到 1M 内存空间。
