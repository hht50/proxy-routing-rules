# Emby 分流规则

统一保留 **两个**规则集：

| 规则集 | 内容 | 客户端策略 |
| --- | --- | --- |
| [Direct.list](Direct.list) | 明确要直连的播放主机 | `DIRECT` |
| [Proxy.list](Proxy.list) | 代理播放线路、Emby 服务入口和接口 | `Emby` |

## 优先级

客户端必须先引用 `Direct.list`，再引用 `Proxy.list`。

- `DOMAIN,a.115cdn.de` 精确走 `DIRECT`
- `DOMAIN-SUFFIX,115cdn.de` 匹配根域名与其他子域，走 `Emby`

`Services.list` 的原有六条规则已完整并入 `Proxy.list`，不再需要单独订阅。客户端中其他早于以上规则的宽泛域名匹配仍可能改变结果，请以实际命中日志为准。

## 使用方式

Surge：

```ini
RULE-SET,https://raw.githubusercontent.com/hht50/proxy-routing-rules/main/Media/Emby/Direct.list,DIRECT
RULE-SET,https://raw.githubusercontent.com/hht50/proxy-routing-rules/main/Media/Emby/Proxy.list,Emby
```

Mihomo：将上述两个 URL 作为 `classical` 规则提供者，依次绑定 `DIRECT`、`Emby`。修改后刷新订阅并重建旧连接。
