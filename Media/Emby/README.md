# Emby 分流规则

| 规则集 | 用途 | 推荐策略 |
| --- | --- | --- |
| [Direct.list](Direct.list) | 映月国内直连主机（精确域名） | `DIRECT` |
| [Services.list](Services.list) | Emby 站点、接口及服务 | `Emby` |
| [Proxy.list](Proxy.list) | 映月代理播放线路 | `Emby` |

## `115cdn.de` 的优先级

- `Direct.list` 使用 `DOMAIN,a.115cdn.de`，该主机必须直连。
- `Proxy.list` 使用 `DOMAIN-SUFFIX,115cdn.de`，覆盖根域名及其余子域名，默认交给 `Emby` 策略。
- **两条规则有意重叠**：客户端按规则顺序先匹配者生效，必须按 `Direct → Services → Proxy` 顺序引用。不要把 `DOMAIN-SUFFIX,115cdn.de,DIRECT` 放在代理规则之前，否则全部子域都会直连。
- Surge 与 Mihomo 其他内联规则中也可能包含 `115cdn.de`；应避免更靠前的宽泛直连覆盖。

## 维护

服务入口与播放线路应分开维护，勿将 Emby 域名放进短剧规则集。现有 [ChinaShortDrama.list](../China/ChinaShortDrama.list) 仍含两条 Emby 直连主机，属于待整理的历史配置。修改后请刷新规则提供者并重新建立播放连接。
