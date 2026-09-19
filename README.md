# mkcloud 专线测评：广港IEPL 3ms实测数据、全套餐价格与优惠码，跨境电商选线不踩坑

搜“mkcloud 专线测评”的人，心里一般绕着三个问题：延迟是不是真有宣传的那么低、一年几千块花得值不值、以及这到底是一条正经专线还是包装出来的二道贩子服务。这篇文章把这三件事一次说清楚：先讲 Mkcloud 的产品形态和合规门槛，再放第三方实测数据，然后把它家目前在售的全部套餐和价格列成表，最后按使用场景给选型建议。

## 先说清楚：MKCloud 是什么，不是什么

Mkcloud 是 2023 年上线的国人商家，卖的是跨境专线 VPS——也就是一台云服务器，配“入口 IP + 出口 IP”两个独立 IPv4。你连上入口机器操作业务，流量从出口 IP 出去，中间走的是 IEPL、IPLC 或 IX 这类专线通道，而不是普通 VPS 的公网路由。

有几件事下单前必须知道，都来自官方购物车页面的原话：

- **需要中国实名**：注册要手机号，购买前要提交姓名、身份证号做一致性验证，企业用户还要营业执照和对公账户。
- **不是机场，也当不了机场**：所有专线产品采用省级白名单，只允许一个省份的 IP 连入入口，防的就是多人共享和违规用途。官方明确禁止机场、翻墙回国等用途，违规清退不退款。
- **出口不能被连入**：这台机器只管“往外访问”，不能拿来建站、收支付回调、收邮件或当游戏服务端。

所以它的定位很清楚：给跨境电商、外贸团队、做 TikTok 直播或需要固定干净出口的个人/企业用的一跳式出海线路。想找翻墙工具的人，看到“省级白名单”这五个字就可以关页面了。

## 线路和延迟：官方标称 vs 第三方实测

Mkcloud 的线路按方向分，官方产品总览给出的端内参考延迟如下：

| 线路方向 | 类型 | 官方端内延迟 | 出口 |
| --- | --- | --- | --- |
| 广港专线 | IEPL | 1~2ms | 香港 BGP |
| 深港 IX 专线 | IX | 1~2ms | 香港 BGP |
| 沪港 IPLC / IX | IPLC / IX | 21ms | 香港 BGP |
| 沪日专线 / IX | IPLC / IX | 25~28ms | 日本 BGP |
| 沪美专线 / IX | IPLC / IX | 124~134ms | 美国 BGP |
| 厦港 / 泉港高防 | 高防 IPLC | 1~2ms | 香港 BGP |
| 上海 CN2 | 国内优化 | — | 上海电信 CN2 |

注意“端内延迟”这个说法：它指的是从国内入口到海外出口这一段，不含你家宽带到入口、以及出口到目标网站的路程。拿它当全程 ping 去对比，会失望。

第三方实测的数据对得上官方口径。vps.dance 对沪日 IPLC 500GB 档的测试显示，上海电信入口的 TCP ping 平均电信 28ms、联通 31ms、移动 33ms，出口落在东京（AS51847 Nearoute），150Mbps 档位单线程能跑到 130Mbps 上下。NodeSeek 上一份针对广港活动机（236 元/月那台）的测评，测得端内延迟 2.05ms，机器是 AMD EPYC 7402P 平台，单核跑分 1613。更早的测评也提到港内 150M 档实际能跑 135~140M。整体看，“广港 3ms 以内、沪日 25ms 上下”这些数字不是纯营销话术。

## 全套餐价格表（当前官网在售）

Mkcloud 的产品分两种计费方式：**流量计费**（共享峰值带宽，流量按上行+下行双向统计，超量停机）和**独享带宽**（带宽独享、不限流量，按 Mbps 付钱）。下面按线路方向把目前在售的档位全部列出，价格为月付原价。

### 广东—香港方向（广港 IEPL，端内 1~2ms）

流量计费，入口默认腾讯广州八线 BGP，出口香港 BGP：

| 套餐 | 配置 | 峰值带宽 | 月流量 | 月付价格 | 购买链接 |
| --- | --- | --- | --- | --- | --- |
| 1TB | 1核2G / 20GB | 200M | 1TB | ¥358 | [ 查看广港IEPL全部档位](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-sh) |
| 2TB | 2核4G / 40GB | 300M | 2TB | ¥568 | [ 查看广港IEPL全部档位](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-sh) |
| 4TB | 2核4G / 40GB | 300M | 4TB | ¥998 | [ 查看广港IEPL全部档位](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-sh) |
| 6TB | 4核8G / 60GB | 500M | 6TB | ¥1388 | [ 查看广港IEPL全部档位](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-sh) |
| 10TB | 4核8G / 60GB | 500M | 10TB | ¥2288 | [ 查看广港IEPL全部档位](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-sh) |
| 20TB | 4核8G / 60GB | 1G | 20TB | ¥4500 | [ 查看广港IEPL全部档位](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-sh) |

说明一点：官方知识库此前写的入门档是 500GB / 228 元，当前商店页展示从 1TB 档起步，入口另有广东移动、电信、联通、三线版本可选，档位结构相同。实际可买档位以下单页为准。

独享带宽版本（2核4G 起步，不限流量）：

| 档位 | 月付价格 | 购买链接 |
| --- | --- | --- |
| 5M 独享 | ¥500 | [ 看广港独享带宽报价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-ex) |
| 10M 独享 | ¥700 | [ 看广港独享带宽报价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-ex) |
| 20M 独享 | ¥1320 | [ 看广港独享带宽报价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-ex) |
| 50M 独享 | ¥3150 | [ 看广港独享带宽报价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-ex) |
| 100M 独享 | ¥5800 | [ 看广港独享带宽报价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-ex) |
| 200M 独享 | ¥11600 | [ 看广港独享带宽报价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-ex) |
| 300M 独享 | ¥17400 | [ 看广港独享带宽报价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-ex) |

再往上还有定制档（更高带宽、可议价）。广东移动入口的 IEPL 独享是另一条产品线：1G 独享 17000 元/月、2G 32000 元/月、5G 75000 元/月，28 核 64G 配置、送独立服务器、含 300Gbps 高防， [👉 查看广东移动独享专线](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-yd-hk-ex)。广东三线版本 200M–2000M 独享也在售，上新参考价 5400 元/月起，现价以产品页为准。

### 深圳—香港方向（深港 IX，端内 1~2ms）

上云互联优化入口，必须搭配云厂前置机使用（阿里云、腾讯云、百度云国内全网及火山云、华为云指定区域等），这也是它比 IEPL 便宜的原因：

| 套餐 | 配置 | 峰值带宽 | 月付价格 | 购买链接 |
| --- | --- | --- | --- | --- |
| 2TB | 2核4G / 40GB | 1G | ¥158 | [ 看深港IXP套餐价格](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-hk-sh) |
| 4TB | 2核4G / 40GB | 1G | ¥258 | [ 看深港IXP套餐价格](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-hk-sh) |
| 6TB | 4核8G / 40GB | 2G | ¥378 | [ 看深港IXP套餐价格](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-hk-sh) |
| 10TB | 4核8G / 40GB | 2G | ¥826 | [ 看深港IXP套餐价格](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-hk-sh) |
| 20TB | 4核8G / 40GB | 2G | ¥1639 | [ 看深港IXP套餐价格](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-hk-sh) |
| 30TB | 4核8G / 60GB | 3G | ¥2458 | [ 看深港IXP套餐价格](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-hk-sh) |
| 50TB | 8核8G / 60GB | 3G | ¥3588 | [ 看深港IXP套餐价格](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-hk-sh) |
| 100TB | 8核16G / 80GB | 5G | ¥7168 | [ 看深港IXP套餐价格](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-hk-sh) |
| 200TB | 8核16G / 80GB | 5G | ¥12288 | [ 看深港IXP套餐价格](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-hk-sh) |
| 300TB | 8核16G / 80GB | 5G | ¥18428 | [ 看深港IXP套餐价格](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-hk-sh) |

原来 3TB/5TB 的档位已升级为 4TB/6TB，带宽提到 1G/2G 峰值。独享版本另有 100M（1600 元）、200M（3000 元）、500M（6000 元）、1G（9000 元）、2G（16000 元）、5G（35000 元）几档， [👉 查看深港独享档位](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-hk-ex)。

### 上海—香港方向（沪港，端内 21ms）

沪港 IPLC 流量计费，上海电信入口：

| 套餐 | 配置 | 峰值带宽 | 月付价格 | 购买链接 |
| --- | --- | --- | --- | --- |
| 1TB | 1核2G / 20GB | 200M | ¥288 | [ 查看沪港IPLC套餐](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-hk-sh) |
| 2TB | 2核4G / 40GB | 300M | ¥428 | [ 查看沪港IPLC套餐](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-hk-sh) |
| 4TB | 2核4G / 40GB | 300M | ¥696 | [ 查看沪港IPLC套餐](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-hk-sh) |
| 6TB | 4核8G / 60GB | 500M | ¥988 | [ 查看沪港IPLC套餐](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-hk-sh) |
| 10TB | 4核8G / 60GB | 500M | ¥1536 | [ 查看沪港IPLC套餐](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-hk-sh) |
| 20TB | 4核8G / 60GB | 1G | ¥3072 | [ 查看沪港IPLC套餐](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-hk-sh) |

独享入门为 2核4G / 40GB / 5Mbps / 不限流量，388 元/月起， [👉 看沪港独享带宽](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-hk-ex)。沪港还有 IXP 上云版本，198 元/月起， [👉 查看沪港IXP档位](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-sh-hk-sh)。

### 上海—日本方向（沪日，端内 25~28ms）

沪日 IPLC 流量计费，上海电信入口：

| 套餐 | 配置 | 峰值带宽 | 月付价格 | 购买链接 |
| --- | --- | --- | --- | --- |
| 1TB | 1核2G / 20GB | 200M | ¥358 | [ 购买沪日IPLC](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-jp-sh) |
| 2TB | 2核4G / 40GB | 300M | ¥568 | [ 购买沪日IPLC](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-jp-sh) |
| 4TB | 2核4G / 40GB | 300M | ¥998 | [ 购买沪日IPLC](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-jp-sh) |
| 6TB | 4核8G / 60GB | 500M | ¥1388 | [ 购买沪日IPLC](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-jp-sh) |
| 10TB | 4核8G / 60GB | 500M | ¥2288 | [ 购买沪日IPLC](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-jp-sh) |
| 20TB | 4核8G / 60GB | 1G | ¥4500 | [ 购买沪日IPLC](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-jp-sh) |

独享版本：5M（600 元）、10M（800 元）、20M（1560 元）、50M（3500 元）、100M（6000 元）、200M（12000 元）、300M（18000 元）每月， [👉 看沪日独享带宽报价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-jp-ex)；再往上是 2–28 核 / 100–5000Mbps 的定制款，起售约 2100 元/月（上新公告口径）。

沪日 IXP 上云版本，同样是云厂前置玩法，1TB 档 166 元/月：

| 套餐 | 配置 | 峰值带宽 | 月付价格 | 购买链接 |
| --- | --- | --- | --- | --- |
| 1TB | 2核4G / 40GB | 200M | ¥166 | [ 看沪日IXP价格](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-jp-sh) |
| 2TB | 2核4G / 40GB | 300M | ¥268 | [ 看沪日IXP价格](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-jp-sh) |
| 3TB | 2核4G / 40GB | 500M | ¥358 | [ 看沪日IXP价格](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-jp-sh) |
| 6TB | 4核8G / 40GB | 1G | ¥688 | [ 看沪日IXP价格](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-jp-sh) |
| 10TB | 4核8G / 40GB | 1G | ¥1125 | [ 看沪日IXP价格](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-jp-sh) |
| 20TB | 4核8G / 40GB | 1G | ¥2150 | [ 看沪日IXP价格](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-jp-sh) |
| 30TB | 4核8G / 60GB | 2G | ¥3165 | [ 看沪日IXP价格](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-jp-sh) |
| 50TB | 8核8G / 60GB | 2G | ¥5222 | [ 看沪日IXP价格](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-jp-sh) |

### 上海—美国方向（沪美，端内 124~134ms）

沪美 IPLC 流量计费，上海电信入口、美国 BGP 出口：

| 套餐 | 配置 | 峰值带宽 | 月付价格 | 购买链接 |
| --- | --- | --- | --- | --- |
| 1TB | 1核2G / 20GB | 200M | ¥428 | [ 选购沪美IPLC套餐](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-us-sh) |
| 2TB | 2核4G / 40GB | 300M | ¥698 | [ 选购沪美IPLC套餐](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-us-sh) |
| 4TB | 2核4G / 40GB | 300M | ¥1258 | [ 选购沪美IPLC套餐](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-us-sh) |
| 6TB | 4核8G / 60GB | 500M | ¥1758 | [ 选购沪美IPLC套餐](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-us-sh) |
| 10TB | 4核8G / 60GB | 500M | ¥2888 | [ 选购沪美IPLC套餐](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-us-sh) |
| 20TB | 4核8G / 60GB | 1G | ¥5666 | [ 选购沪美IPLC套餐](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-us-sh) |

沪美 IXP 上云版本：1TB / 200M 峰值 266 元/月起，往上有 2TB（430 元）、3TB（615 元）、6TB（1166 元）、10TB（1945 元）、20TB（3686 元）、30TB（5529 元）、50TB（9216 元）， [👉 查看沪美IXP套餐](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-us-sh)。美国方向独享款 100–5000Mbps 起售约 3400 元/月。

### 福建高防与上海 CN2

厦港高防 IPLC（厦门 BGP 入口，端内 1~2ms，默认 100Gbps 高防，无跨省 QoS、无省份白名单限制）：

| 档位 | 配置 | 月付价格 | 购买链接 |
| --- | --- | --- | --- |
| 200M 独享 | 4核8G / 40GB | ¥6000 | [ 查看高防专线报价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fxm-hk-ex) |
| 500M 独享 | 8核8G / 60GB | ¥13500 | [ 查看高防专线报价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fxm-hk-ex) |
| 1G 独享 | 28核64G / 512GB，送独立服务器 | ¥24000 | [ 查看高防专线报价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fxm-hk-ex) |
| 2G 独享 | 28核64G / 512GB | ¥46000 | [ 查看高防专线报价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fxm-hk-ex) |
| 5G 独享 | 28核64G / 512GB | ¥110000 | [ 查看高防专线报价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fxm-hk-ex) |

泉港版本（泉州电信入口）200M–5000M 独享在售，4200 元/月起；上海 CN2 是国内优化产品（上海动态联通入口、上海电信 CN2 出口），500M 独享 4500 元/月，8核16G 配置，7 天内交付。这两条线在商店里选对应的地区入口即可， [👉 去商店按线路筛选](https://bit.ly/MKCLoud)。

## 独享带宽值不值这笔钱

把广港独享的档位换算成单价，规律很直白：5M 档折合 100 元/M，100M 档 58 元/M，300M 档降到约 58 元以下、大带宽档更低。带宽越大单价越便宜，但起跳门槛就是 500 元/月。

什么时候需要独享？长时间推流、持续传输备份、对速率稳定性有硬要求的场景。共享套餐的“200M 峰值”是指最高能冲到的速率，不保证晚高峰持续跑满；独享是全天候锁死的速率，不限流量。如果你只是白天操作店铺后台、偶尔传素材，流量计费便宜得多；如果是 24 小时直播推流，独享才划算。

## 优惠码和活动：能省多少，怎么省

Mkcloud 的促销节奏基本跟着节假日走，春节、五一、618、双旦都有活动。从官方知识库的活动回顾看，有几个码反复出现：

- **MK-8.8**：流量计费产品全场 88 折循环，多场活动复用过，算是“常客码”；
- **MK-7.8**：独享带宽产品首月 78 折，同样多次出现；
- **MK-IEPL-WELCOME / MK-IPLC-WELCOME**：IEPL / IPLC 系列循环 9 折，商家早期上线时就存在，第三方优惠汇总目前仍列为可用；
- **IXCLOUD / US-6.9 / JP-7.7**：IXP 上新活动码，力度到 6.9 折；
- **CLOUD-2T-NEW**：上云互联 2TB 档限时码，用过 8 折（158 元折到 126 元）。

两点提醒。第一，这些码都绑定具体活动期，活动结束就失效，最稳的做法是在购物车的“优惠劵码”框里填一下，登录后系统会显示对当前商品有效的券——无效码会直接报错，不会有副作用。第二，别指望付款周期本身有折扣：官方知识库给的沪港共享入门例子，月付 288、季付 864、年付 3456，就是简单的整数倍，长周期不自带优惠。真正的省钱路径是活动码加上老客权益（同一产品持满 6 个月可返现一个月月费的代金券）。

## 购买流程和几道门槛

实际下单路径不复杂：手机号注册账号，先做实名认证（姓名+身份证号，审核通过才能正常购买），然后进商店选地区、网络入口、计费类型和套餐档位。直连款要选“可连入省份”——开通后只允许该省的 IP 连入口，之后可以改绑其他省份。付款支持支付宝，现货一般一分钟内自动开通，独享定制款和上海 CN2 例外（CN2 明确 7 天内交付）。

IXP 产品多一道前置：你得先有一台支持范围内的云厂机器（阿里云、腾讯云、百度云国内全网，火山云、华为云、UCloud 的指定区域），通过它的网络连入专线。已经有云上业务的团队几乎零成本；纯个人用户要额外算这笔前置费用。还有一件事值得记住：**退款只认质量问题**，需要提交具体的延迟、速度数据做证据，审核通过才退，开通后不支持换地域——所以先月付试水是这类商家的标准用法，2023 年最早的第三方测评就把“只建议月付”写进了结论。

## 第三方口碑汇总

把能查到的公开测评放在一起看，评价画风比较一致。2023 年底商家刚起步时，测评圈给广港线路的评价是“过于便宜”“买 BGP IP 送专线”，IP 纯净度测试中欺诈评分拿到 0 分，同时提醒新商家存续风险、建议月付。2025 年初 NodeSeek 上的活动机实测（2核4G / 268M / 666GB 那台）确认了端内 2ms 级延迟和正常的机器性能，也如实记录了流媒体解锁一般、个别平台把 IP 识别为数据中心的问题。2026 年的几篇汇总类测评则提到实测速率能到标称峰值的九成上下、晚高峰能维持三位数速率、在线率接近 99.99%——这些是各测评自己的监控口径，看看量级就好。

官方 Telegram 通知群保持活跃，维护提前公告（比如 4 月那次约 30 分钟的计划性停机）、活动、IP 变更都会推送，这对判断商家运营状态是个正向信号。客服高峰期响应慢是多篇测评共同提到的短板，处理技术问题直接提工单更快。

## 下单前的短板清单

价格之外，这几个限制值得掂量：

- **无 SLA 承诺**，官方不保证无中断或固定恢复时长；
- **流量双向计费**，标 1TB 实际可用量要按上下行总和算，超量直接停机，需购买流量重置或升级套餐；
- **出口是机房 IP**，不保证原生、不保证流媒体解锁，独享 IP 也不承诺平台账号永不风控；
- **2023 年成立的商家**，跑路风险需要自己评估，这也是“先月付”的另一个理由；
- **共享带宽是峰值**，对持续速率有执念的话请直接看独享档。

## 按场景选型：对号入座

- **TikTok 直播 / 东南亚店铺**（华南用户）：广港 IEPL 1TB 档 358 元/月起；深圳周边且手上已有云厂机器的，深港 IXP 2TB 档 158 元/月是全店最便宜的入门价。
- **日本电商、AI API 访问**：沪日 IPLC 1TB 358 元/月；要压成本且能用云厂前置，沪日 IXP 1TB 166 元/月。
- **美区亚马逊、PayPal 等业务**：沪美 IPLC 1TB 428 元/月，或沪美 IXP 1TB 266 元/月。
- **上海及长三角办公**：沪港 IPLC 1TB 288 元/月，21ms 端内延迟对日常操作足够顺滑。
- **游戏、金融类需要高防大带宽的**：直接看厦港/泉港独享，6000 元/月起，属于企业预算范围。
- **只需要国内优化线路**：上海 CN2 500M 独享 4500 元/月，先提交工单确认交付周期。

拿不准的话，从月付 + 最小档位开始，用一周真实业务流量验证再决定要不要加档， [👉 进商店看当前实时价和库存](https://bit.ly/MKCLoud)。

## 常见问题

**MKCloud 是机场吗？** 不是。它是交付 VPS 的专线服务商，明确禁止机场、翻墙回国用途，省级白名单机制也从产品层面堵住了多人共享。

**流量是双向算的吗？** 是。按上行+下行合计统计，超量停机，可自助购买流量重置或工单升级。

**能几个人共用一台吗？** 白名单只允许一个省份的 IP 连入，小团队在同一城市用没问题，跨省共用做不到。

**可以建站吗？** 不行。出口不接受外部连入，建站、支付回调、邮件接收都不支持。

**出问题能退款吗？** 仅限质量问题，需要提交具体延迟/速度数据做证据，由商家审核；开通后不能换地域。

**买月付还是年付？** 长周期不自带折扣，年付只在确认线路稳定、且活动码给力时才划算。第一次买，月付。
