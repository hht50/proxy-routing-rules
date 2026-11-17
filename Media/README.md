# Media · 媒体分流规则总目录

按地区与用途维护媒体规则；规则文件仅包含匹配条件，出口由 Surge / Mihomo 客户端决定。

| 子目录 | 规则与用途 |
| --- | --- |
| [China](China/) | [ChinaShortDrama.list](China/ChinaShortDrama.list)：大陆短剧、直播及历史直连条目 |
| [Japan](Japan/) | [JapanMedia.list](Japan/JapanMedia.list)：日本影视、电视、动画、音乐 |
| [Korea](Korea/) | [KoreaMedia.list](Korea/KoreaMedia.list)：韩国影视、直播、电视 |
| [Vietnam](Vietnam/) | [VietnamMedia.list](Vietnam/VietnamMedia.list)：越南影视、电视、音乐、动漫 |
| [Emby](Emby/) | [Direct.list](Emby/Direct.list)、[Proxy.list](Emby/Proxy.list)：直连与代理（含服务入口） |
| [Proxy](Proxy/) | [Proxy.list](Proxy/Proxy.list)：其他媒体代理 |
| [Metadata](Metadata/) | [TMDB.list](Metadata/TMDB.list)、[Trakt.list](Metadata/Trakt.list)、[Lyrics.list](Metadata/Lyrics.list) |
| [Social](Social/) | [TikTok.list](Social/TikTok.list) |
| [Adult](Adult/) | 成人媒体独立规则，详见 [README](Adult/README.md) |
| [Global](Global/) | [说明](Global/README.md)：国际媒体与待分类内容 |

## 规则优先级与维护

1. Surge、Mihomo 都按规则顺序先匹配者生效；专用媒体规则应尽量位于宽泛 GEOIP / 综合规则之前。
2. Emby 必须先引用 `Direct.list`，再引用 `Proxy.list`。`a.115cdn.de` 精确直连，其余 `115cdn.de` 子域由代理规则匹配。
3. 韩国规则统一使用 `Media/Korea/KoreaMedia.list`；`HanXiaoQuan.list` 已删除。
4. 地区媒体规则的范围可能与综合规则重叠；实际命中应通过客户端连接记录验证。
5. 规则文件不写具体策略或节点；修改后刷新规则提供者并断开旧连接重新测试。
