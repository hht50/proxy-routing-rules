# Media · 媒体分流规则总目录

所有媒体相关规则统一从本目录维护，按出口地区和业务类型组织。

## 目录结构

| 子目录 | 内容 | 主要入口 |
| --- | --- | --- |
| [China](China/) | 中国大陆直连：短剧、悦听吧、体育直播、Emby 直连域名 | [ChinaShortDrama.list](China/ChinaShortDrama.list) |
| [Japan](Japan/) | 日本媒体 | [JapanMedia.list](Japan/JapanMedia.list) |
| [Korea](Korea/) | 韩国媒体：韩小圈、SOOP | [HanXiaoQuan.list](Korea/HanXiaoQuan.list) |
| [Proxy](Proxy/) | 观影优选 / 代理自选出口 | [Proxy.list](Proxy/Proxy.list) |
| [Global](Global/) | 国际媒体及待分类旧规则 | [说明](Global/README.md) |
| [Emby](Emby/) | Emby 服务、国内直连与代理播放线路 | [说明](Emby/README.md) |
| [Metadata](Metadata/) | TMDB、Trakt、歌词服务 | [说明](Metadata/README.md) |
| [Social](Social/) | TikTok 等媒体社交平台 | [说明](Social/README.md) |
| [Adult](Adult/) | 成人媒体通用规则、越南版 | [说明](Adult/README.md) |

## 维护约定

1. **按出口策略汇总**：中国大陆、日本、韩国、Proxy 各自维护统一规则集，不再为每个站点新建独立策略规则。
2. **业务子目录用于收纳**：Emby、Metadata、Social、Adult 为媒体专项规则；不能仅凭目录位置决定出口，仍需由客户端指定策略。
3. 规则集仅保存匹配条件，不把 `DIRECT` 或具体节点写入域名行。
4. 本次为安全迁移，**旧路径暂时保留兼容订阅**；新子目录中的历史文件是迁移副本，不会与旧路径自动同步。待 Surge、Mihomo/OpenClash 全部引用新地址后再清理旧文件。
5. SOOP 的 `sooplive.com` 已加入韩国主规则集；[SOOP-Legacy.list](Korea/SOOP-Legacy.list) 仅为历史扩展规则备份，未全部合并进主规则。
