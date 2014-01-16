一个电商 Crawler （类etao）
=

##SCUT - Otto Lu

###已实现功能

####基本要求：
* (已实现) 这是web应用，页面上需要有个输入框，用户输入商品确定后，返回商品列表。
* (已实现) 列表的合并，展现等逻辑，在前端浏览器处理。
* (已实现) 用http代理服务器进行跨域拉取各大电商网站的搜索列表，建议用nodejs写代码搭建，逻辑简单
* (已实现) 最后合并的搜索列表，应该是一个按价格从低到高的混排列表，每一项需要标明来自哪个网站，用户可以点击跳到原页面浏览
* (已实现) 可在chrome开发，兼容webkit即可
* (已实现) 抓取的电商网站： taobao, paipai, 360buy

####可选优化：
* (已实现) 列表要去掉一个不合理的结果，比如，搜索iphone5, 会有些iphone配件出现，这不是用户想要的（提示：可以根据价格过低过高等策略去掉一些不合理的结果）
* (不评价) 商品列表每一项的展现需要统一，并美观
* (未完全测试) 应用兼容主流的浏览器
* (已实现) 并发拉取，并行处理，提高搜索速度

###运行环境
* Ubuntu 12.04 LTS
* Nodejs 0.10.4
* ejs @0.8.3 / express @3.1.0 / generic-pool @2.0.2 / iconv-lite @0.2.7 /
  jsdom @0.5.5 / zlib @1.0.5

###Buglist(已知)
* 搜索中文词条时，低概率返回结果不全
* 京东价格为图片，未作图片解析为文字的处理
* 爬取拍拍时，使用hack手段去重定向到正确的地址，效率不够高
* 为了用户体验，设置获取超时为10s，可能使结果不够多
* 京东和淘宝爬取速度较为正常，拍拍为短板
* （更新中～）


