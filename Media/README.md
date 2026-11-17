# Media 媒体规则 · 地区索引

## 地区目录

| 地区 | 目录 | 当前规则 |
| --- | --- | --- |
| 🇯🇵 日本 | [Japan](Japan/) | [日本媒体](Japan/JapanMedia.list)、[黄果](Japan/HuangGuo.list) |
| 🇰🇷 韩国 | [Korea](Korea/) | [韩小圈](Korea/HanXiaoQuan.list) |
| 🇨🇳 中国大陆 | [China](China/) | [中国短剧](China/ChinaShortDrama.list)、[悦听吧主站](China/YueTingBa.list) |
| 🌐 国际 / 待分类 | [Global](Global/) | [成人媒体通用](Adu)、[成人媒体越南版](Adu-vietnam.list) |
| 🔀 代理 · 自选出口 | [Proxy](Proxy/) | [XifanACG 追番](Proxy/XifanACG.list)、[悦听吧图片](Proxy/YueTingBa-Images.list) |

## 维护约定

1. 新增媒体规则优先放入 `Media/<Region>/<Service>.list`；不绑定地区的代理影视资源放 `Media/Proxy/`，每个服务独立文件。
2. 规则集只写域名/IP 匹配条件，出口策略由 Surge、Mihomo、OpenClash 各自配置。
3. 旧路径仍保留以避免已有订阅失效。**目前新旧路径为独立副本，不会自动同步**；完成客户端迁移前，修改已有规则需同步更新两处。
4. 按服务地区归类；需要代理但允许自行选择出口的放 `Proxy`，地区未知且未明确代理用途的放 `Global`。黄果按日本出口需求暂归日本目录。
5. 不将越南版成人规则误认为网站属于越南；未来可按需求增加 Vietnam、Taiwan、HongKong 等目录。
6. 同一域名可能出现在不同服务的专用集合中，需以客户端规则优先级确定最终策略。
