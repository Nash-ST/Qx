# name=番茄小说去广告（精简稳定版）
#!desc=去除开屏广告、阅读页短剧、统计上报，保留阅读、评论、金币、排行榜、插图、抖音登录
#!author=ChatGPT
#!homepage=https://github.com/changzhaoCZ/fqnovel-adrules
#!version=1.0

[rewrite_local]

# 广告SDK

^https?://mssdk.zijieapi.com/.* url reject
^https?://feedback-c.zijieapi.com/.* url reject
^https?://mon.snssdk.com/.* url reject
^https?://mon.zijieapi.com/.* url reject
^https?://toblog.ctobsnssdk.com/.* url reject
^https?://polaris.zijieapi.com/.* url reject

# 数据采集

^https?://dig.zjurl.cn/.* url reject
^https?://dig.bdurl.net/.* url reject
^https?://.*applog.*/.* url reject

# 广告投放

^https?://ads.*.zijieapi.com/.* url reject
^https?://gecko.*.zijieapi.com/.* url reject

# 阅读页短剧

^https?://lf.*-webcast-cdn-tos-ncdn.bytegecko.com/.* url reject
^https?://bsync3-normal-hl.zijieapi.com/.* url reject
^https?://p\d+.douyinpic.com/.* url reject
^https?://ecombdimg.com/.* url reject

# 番茄统计

^https?://mon.*-misc-.*.fqnovel.com/.* url reject

[mitm]

hostname = %APPEND% mssdk.zijieapi.com,feedback-c.zijieapi.com,mon.snssdk.com,mon.zijieapi.com,toblog.ctobsnssdk.com,polaris.zijieapi.com,dig.zjurl.cn,dig.bdurl.net
