# Media 媒体规则 · 按出口策略分类

| 分类 | 统一规则集 | 推荐客户端策略 | 内容 |
| --- | --- | --- | --- |
| 🇨🇳 中国大陆 | [China/ChinaShortDrama.list](China/ChinaShortDrama.list) | DIRECT | 国内短剧、悦听吧主站等 |
| 🇯🇵 日本 | [Japan/JapanMedia.list](Japan/JapanMedia.list) | 日本节点策略 | 日本媒体、黄果等 |
| 🇰🇷 韩国 | [Korea/HanXiaoQuan.list](Korea/HanXiaoQuan.list) | 韩国节点策略 | 韩小圈、SOOP 韩国直播等 |
| 🔀 代理 | [Proxy/Proxy.list](Proxy/Proxy.list) | 观影优选 / PROXY | XifanACG、悦听吧图片等 |
| 🌐 国际 / 待分类 | [Global](Global/) | 按实际用途 | 尚未合并的通用媒体规则 |

## 维护约定

1. **同一出口策略共用一个规则集**，新增域名追加到对应主规则文件，不为单个网站新建订阅文件。
2. 规则集只包含匹配条件；DIRECT、日本、韩国、观影优选等策略由客户端指定。
3. 不同出口必须拆分，不能将 `yuetingba.cn`（直连）与 `images.weserv.nl`（代理）放入同一集合。
4. 旧独立文件暂时保留兼容历史订阅，未来逐步迁移客户端引用。旧文件与主规则集不自动同步。
5. 共享 CDN 域名可能影响其他网站，新增前应核对匹配范围与规则优先级。
