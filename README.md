# weiboCrawler-Simple
运用Python通过微博m站的接口简单获取指定用户的微博数据，包括内容、话题、链接、评论点赞转发等 

测试有效时间2018-08-04

## 功能介绍
1. 爬取指定user_id的所有微博基本内容并保存至csv
2. 提取微博中的话题标签，以及微博中的链接
3. 语言环境 Python3

## 使用方法
1. 打开`weiboCrawler/crawling.py`文件，修改里面的配置信息

	```
	# 配置-根据自己需要进行修改
	# 需要爬取的用户的微博id https://weibo.com/u/5203786516?refer_flag=1001030101_
	uid = '5203786516'
	
	# 从第几页开始爬取
	page_index = 1
	
	# 代理启用开关
	proxy_valid = False
	
	# 设置代理ip池 可去http://www.xicidaili.com找，对应http 和 https
	proxy_pool = {
	    'http': [
	        '61.135.217.7:80',
	        '118.190.95.35:9001',
	    ],
	
	    'https': [
	        '124.42.68.152:90',
	        '118.190.145.138:9001',
	        '27.184.127.65:8118',
	    ]
	}
	
	# 数据默认保存目录
	file_path = '../../weibo output'
	
	# 抓取时间间隔，最好不要低于0.5，防止被封
	interval = 1
	
	```
2. 运行	`crawling.py` 文件（可用PyCharm运行）
3. 结果将保存在`file_path`目录中，文件名为`uid_时间戳.csv`
4. 数据格式为

	```
	微博id, 微博地址, 发布时间, 微博内容, 话题, 链接, 链接名字, 链接有效性, 点赞, 评论, 转发
	
	```
	
## TODO
- 为解决朋友工作需要，临时学的Python来写的此项目，放上来帮助有相同需要的朋友

- 暂时没有下一步计划，有其他需求的朋友可以提
