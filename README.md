# 分流

自用的 Quantumult X 分流规则（`filter_remote` 远程规则）。

## 规则列表

| 文件 | 用途 | 规则数 | 订阅链接 |
| --- | --- | --- | --- |
| Emby | Emby 媒体服务器 | 9 | [raw](https://raw.githubusercontent.com/AT-MA/fenliu/main/Emby) |
| EmbyProxy | 需要走代理的 Emby 服务器 | 11 | [raw](https://raw.githubusercontent.com/AT-MA/fenliu/main/EmbyProxy) |
| okx | OKX 交易所 | 8 | [raw](https://raw.githubusercontent.com/AT-MA/fenliu/main/okx) |
| bybit | Bybit 交易所 | 9 | [raw](https://raw.githubusercontent.com/AT-MA/fenliu/main/bybit) |
| bitget | Bitget 交易所 / BitKeep 钱包 | 4 | [raw](https://raw.githubusercontent.com/AT-MA/fenliu/main/bitget) |
| Gate | Gate.io 交易所 | 11 | [raw](https://raw.githubusercontent.com/AT-MA/fenliu/main/Gate) |
| mexc | MEXC 交易所 | 8 | [raw](https://raw.githubusercontent.com/AT-MA/fenliu/main/mexc) |
| Weex | WEEX 交易所 | 3 | [raw](https://raw.githubusercontent.com/AT-MA/fenliu/main/Weex) |
| 币市 | BitMart 交易所 | 6 | [raw](https://raw.githubusercontent.com/AT-MA/fenliu/main/%E5%B8%81%E5%B8%82) |
| 米哈游 | 米哈游 / HoYoverse 游戏（直连） | 12 | [raw](https://raw.githubusercontent.com/AT-MA/fenliu/main/%E7%B1%B3%E5%93%88%E6%B8%B8) |

## 使用方法

在 Quantumult X 配置的 `[filter_remote]` 中添加，例如：

```ini
[filter_remote]
https://raw.githubusercontent.com/AT-MA/fenliu/main/okx, tag=OKX, force-policy=代理, update-interval=86400, opt-parser=false, enabled=true
```

建议用 `force-policy` 指定策略，规则文件里写的策略名只作备注。

## 格式约定

- 每行一条：`类型,值[,策略]`，逗号两边不留空格
- 类型统一小写：`host`、`host-suffix`、`host-keyword`、`ip-cidr`
- 以 `#` 开头的行是注释
- 文件名就是订阅地址的一部分，**不要改名**，否则已有订阅会失效
