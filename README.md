# nvme vps：RackNerd 年付 21.99 美元起的全套餐对比，机房、续费规则与选配建议一次讲清

搜 "nvme vps" 的人，多半卡在同一个问题上：想要磁盘快、网络不缩水的 VPS，预算却只有每月几美元。市面上宣传 NVMe 的便宜 VPS 很多，价格从 2 美元到 5 美元一个月都有，配置表五花八门，续费规则更少有人写清楚。

这篇以 RackNerd 为例，把它在售的三条 KVM VPS 产品线共 19 个套餐全部列出来，算清首年和续费的真实成本，说清它的磁盘到底是什么规格，以及哪些人适合买、哪些人该看看别家。

> **选购速览**：冲着 NVMe 来、想低成本试水，选 Ryzen NVMe 线的 512 MB 年付套餐，$26.99/年，折合每月约 $2.25；要全站最低年付价、跑 n8n/Coolify 这类自托管应用，选特价线的 1 GB KVM，$21.99/年且官方承诺续费同价。👉 [开通 512 MB Ryzen NVMe 年付套餐](https://my.racknerd.com/aff.php?aff=11397&pid=500)

## RackNerd 有没有真正的 NVMe VPS？

有，对应的是 Ryzen 线。这条产品线采用 AMD Ryzen 3900X 处理器，存储为纯 NVMe RAID-10 阵列，KVM 虚拟化，1Gbps 端口，下单后即时开通。RackNerd 同时还有两条以 SSD 为口径的产品线（洛杉矶 Xeon 线和年付特价线），价格体系接近，但官方页面没有为它们标注 NVMe 规格。

也就是说，NVMe 在 RackNerd 是按产品线区分的，不是全系标配。第三方测评对 Ryzen 线的磁盘表现描述比较一致：RAID-10 阵列，`dd` 写入测试在 700–900 MB/s 区间，磁盘 I/O 标称高于 1 GB/s。这些数字出自第三方指南，官方页面没有给出具体跑分承诺，下单后用 `fio` 自己验证一遍最稳妥。

还有一点值得留意：第三方指南记录 RackNerd 过去推出过 Ryzen 7950X（DDR5 内存 + Gen4 NVMe）的限量年付特惠，售完即止、等下一次季节性活动补货。这类库存型特惠是否在售，下单前以官网 specials 页为准。

## 全套餐配置与价格对比

RackNerd 官网当前展示三条 KVM VPS 产品线：主打 NVMe 的 Ryzen 线、按月计费为主的洛杉矶 Xeon 线、年付锁价的特价线。三张表如下，所有套餐均含完整 root 权限、1 个 IPv4 和 1Gbps 端口。

**Ryzen NVMe 线（Ryzen 3900X + 纯 NVMe，即时开通）**

| 套餐 | vCPU | NVMe 存储 | 月流量 | 价格 | 购买 |
| --- | --- | --- | --- | --- | --- |
| 512 MB | 1 核 | 10 GB | 500 GB | $26.99/年（唯一按年计费档） | [ 开通 512 MB NVMe](https://my.racknerd.com/aff.php?aff=11397&pid=500) |
| 1 GB | 1 核 | 15 GB | 1 TB | $17.99/月 | [ 开通 1 GB NVMe](https://my.racknerd.com/aff.php?aff=11397&pid=501) |
| 2 GB | 2 核 | 20 GB | 2 TB | $20.59/月 | [ 开通 2 GB NVMe](https://my.racknerd.com/aff.php?aff=11397&pid=502) |
| 4 GB | 2 核 | 30 GB | 3 TB | $24.59/月 | [ 开通 4 GB NVMe](https://my.racknerd.com/aff.php?aff=11397&pid=503) |
| 6 GB | 3 核 | 45 GB | 4 TB | $27.59/月 | [ 开通 6 GB NVMe](https://my.racknerd.com/aff.php?aff=11397&pid=504) |
| 8 GB | 3 核 | 75 GB | 5 TB | $36.59/月 | [ 开通 8 GB NVMe](https://my.racknerd.com/aff.php?aff=11397&pid=505) |
| 12 GB | 4 核 | 90 GB | 6 TB | $55.99/月 | [ 开通 12 GB NVMe](https://my.racknerd.com/aff.php?aff=11397&pid=506) |

**洛杉矶 KVM 线（Asia Optimized Network，Intel Xeon + RAID-10 SSD，注意与 Ryzen 线的核数、磁盘口径不同）**

| 套餐 | vCPU | SSD 存储 | 月流量 | 价格 | 购买 |
| --- | --- | --- | --- | --- | --- |
| 512 MB | 1 核 | 30 GB | 500 GB | $26.99/年 | [ 开通年付 512 MB](https://my.racknerd.com/aff.php?aff=11397&pid=1) |
| 1 GB | 2 核 | 50 GB | 1 TB | $17.99/月 | [ 开通 1 GB 套餐](https://my.racknerd.com/aff.php?aff=11397&pid=20) |
| 2 GB | 3 核 | 75 GB | 2 TB | $20.59/月 | [ 开通 2 GB 套餐](https://my.racknerd.com/aff.php?aff=11397&pid=21) |
| 4 GB | 4 核 | 130 GB | 3 TB | $24.59/月 | [ 开通 4 GB 套餐](https://my.racknerd.com/aff.php?aff=11397&pid=22) |
| 6 GB | 5 核 | 170 GB | 4 TB | $27.59/月 | [ 开通 6 GB 套餐](https://my.racknerd.com/aff.php?aff=11397&pid=23) |
| 8 GB | 6 核 | 220 GB | 5 TB | $36.59/月 | [ 开通 8 GB 套餐](https://my.racknerd.com/aff.php?aff=11397&pid=24) |
| 12 GB | 7 核 | 300 GB | 6 TB | $55.99/月 | [ 开通 12 GB 套餐](https://my.racknerd.com/aff.php?aff=11397&pid=25) |

**年付特价 KVM 线（KVM/ctrl 面板，可多机房部署，官方承诺续费同价）**

| 套餐 | vCPU | SSD 存储 | 月流量 | 年付价格 | 购买 |
| --- | --- | --- | --- | --- | --- |
| 1 GB | 1 核 | 20 GB | 3 TB | $21.99/年 | [ 开通 1 GB 特价机](https://my.racknerd.com/aff.php?aff=11397&pid=952) |
| 2 GB | 2 核 | 35 GB | 5 TB | $35.99/年 | [ 开通 2 GB 特价机](https://my.racknerd.com/aff.php?aff=11397&pid=953) |
| 4 GB | 3 核 | 60 GB | 7 TB | $59.99/年 | [ 开通 4 GB 特价机](https://my.racknerd.com/aff.php?aff=11397&pid=954) |
| 6 GB | 6 核 | 100 GB | 12 TB | $89.99/年 | [ 开通 6 GB 特价机](https://my.racknerd.com/aff.php?aff=11397&pid=955) |
| 8 GB | 7 核 | 150 GB | 20 TB | $119.99/年 | [ 开通 8 GB 特价机](https://my.racknerd.com/aff.php?aff=11397&pid=956) |

三条线的取舍各不相同。同价位下洛杉矶 Xeon 线给的核数和磁盘最多（2 GB 档就有 3 核 75 GB），但磁盘是 SSD 口径；Ryzen 线磁盘小一些，换来的是纯 NVMe 的 I/O 和 3900X 的单线程性能；特价线年付锁价、流量最大，存储和 CPU 最少。认准 NVMe 就看第一张表，认准磁盘容量和月付灵活性看第二张，认准总成本看第三张。

## 真实成本：首年花多少，续费会不会涨

特价线续费同价，官方原话是 "lifetime recurring"——只要保留服务，续费价格和首购一致。1 GB 特价机三年总成本就是 $21.99 × 3 = $65.97，折合每月 $1.83，不存在首年低价、次年翻倍的套路。

Ryzen 线和洛杉矶线的月付套餐，官方页面没有标注同等的续费承诺，这两条线按月计费，不续费直接停就行，风险可控。年付档里，Ryzen 512 MB 套餐 $26.99/年折合约 $2.25/月，和官网首页 "VPS from $2.24/mo" 的起价口径基本对应（官网起价可能对应其他促销套餐，下单前以购物车实价为准）。

阶梯差价也有讲究。Ryzen 线 1 GB 到 2 GB 只差 $2.60/月，内存翻倍、多一个核，是全表性价比最陡的一段；2 GB 到 4 GB 差 $4/月，存储从 20 GB 加到 30 GB，但核数不变，值不值看你缺内存还是缺磁盘。洛杉矶线支持升级到上一档，重启约一分钟生效，可以先买小的不够再升。

## 机房怎么选：亚洲用户优先洛杉矶

RackNerd 全球有 20 个机房：北美覆盖 Los Angeles、San Jose、Seattle、Dallas、Chicago、Utah、New York、Ashburn、Atlanta、Toronto、Tampa 等，欧洲有 Amsterdam、London、Dublin、Strasbourg。洛杉矶线路官方标注为 Asia Optimized Network，走亚洲优化出口，对中国和亚太方向延迟更友好。第三方指南的建议一致：亚洲用户选 Los Angeles 或 San Jose，欧洲用户选 Amsterdam 或 Strasbourg，美东业务选 New York 或 Ashburn。

IPv6 是个容易被忽略的条件：洛杉矶和法国机房可免费申请最多 100 个 IPv6 地址，下单后开工单即可，其他机房暂不支持。需要 IPv6 做测试或反代的读者，这一条基本决定了机房选项。

库存按硬件情况轮换，不是每个机房随时都有每档套餐。某个位置售罄时，通常只能换档或等补货。

## 同价位竞品大概什么行情

"nvme vps" 搜索结果里常见的几个对手，官网挂出的起价大致是：Terranode 的 NVMe VPS 每月 2.99 美元起（5 个区域可选），Sharktech 的 NVMe VPS 每月 3.98 美元起，主打 DDoS 防护；AlphaVPS 的 EPYC 加 NVMe 方案每月 4.24 欧元起。这些都是各家官网的起价口径，具体配置和流量要进套餐页才能确认。

RackNerd 在这场比较里的位置：年付折算月价更低（$1.83–$2.25），机房数量多，但 Ryzen 线的 NVMe 规格主要靠第三方指南佐证。厂商必须在产品名里写明 NVMe、或需要 DDoS 防护的读者，Sharktech 和 AlphaVPS 这类对口一些；要低价、大流量和续费确定性，RackNerd 的特价线和 Ryzen 年付档更有优势。

## 这些限制下单前要知道

**没有退款政策。** 第三方指南明确写了 RackNerd 不提供退款。想验证线路和性能，从最便宜的年付档入手——Ryzen 512 MB 或特价 1 GB 都行，别第一天就上大套餐。

**全部是非托管（unmanaged）服务。** 平台问题有 24/7 支持，服务器里装什么、怎么配、坏了怎么修都是自己的事。没有运维经验又需要有人管服务器的，这个产品线不适合你。

**512 MB 内存跑不动 WordPress。** 官方一键应用目录里门槛最低的 n8n 和 Coolify 也要 2 GB 内存，512 MB 档的合理用途是轻负载场景——第三方指南列了 DNS 从节点、静态小站、WireGuard 端点、状态页这类例子。拿它装 WordPress 容易 OOM。

**特价机的 1 GB 档同理。** 3 TB 流量很充裕，但 1 GB 内存能干的事有限，当轻量代理或状态页主机合理，当小型应用服务器就勉强了。

## 跑 AI 和自托管应用，多少内存才够

这是 RackNerd 特价页 FAQ 写得很实在的一组门槛，直接决定你该买哪档：

- **OpenClaw：至少 8 GB 内存**，对应 $119.99/年的 8 GB 档
- **Hermes Agent、AnythingLLM、Ollama、LibreChat：至少 4 GB**，对应 $59.99/年的 4 GB 档
- **n8n、Coolify：2 GB 起就够**，对应 $35.99/年的 2 GB 档

这些应用都能在 ctrl 面板里一键安装，装好后凭据直接显示在面板内。选套餐的顺序应该反过来：先确定要跑什么应用，按内存门槛倒推套餐，再看价格能不能接受。想跑本地 LLM（Ollama）却买了 1 GB 档，等于白花钱。

打算先跑个 n8n 或 Coolify 试试自动化的，2 GB 档是最低门槛：👉 [开通 2 GB 年付特价机（$35.99/年）](https://my.racknerd.com/aff.php?aff=11397&pid=953)

## 常见问题

**RackNerd 续费会涨价吗？** 特价线不会，官方明确 lifetime recurring、续费同价。Ryzen 线和洛杉矶月付线没有同等的官方承诺，按月计费随时可停，影响有限。

**能装什么系统？** 特价线支持 CentOS、Rocky Linux、AlmaLinux、Fedora、Debian、Ubuntu，也可通过工单申请自定义 ISO 安装。ctrl 面板随时可重装系统、切换发行版。

**支持 IPv6 吗？** 支持，但仅限洛杉矶和法国机房，下单后开工单申请，最多 100 个免费地址。

**能跑 Docker、WordPress 吗？** 能。ctrl 里可一键装 Docker + Portainer，WordPress 有 AdminBolt、CyberPanel、CloudPanel 三个一键方案；有完整 root 权限，自定义栈随便折腾。

## 按你的用途选

- 认准 NVMe、先低成本试水 → Ryzen 512 MB 年付，$26.99/年
- 跑 n8n、Coolify、轻量应用，要续费确定性 → 特价 2 GB 档，$35.99/年，续费同价
- 正经的 WooCommerce 站或小数据库，要大磁盘 → 洛杉矶 4 GB 档，$24.59/月，4 核 130 GB SSD
- 本地跑 Ollama、AnythingLLM → 特价 8 GB 档，$119.99/年，内存门槛在这里
- 必须要厂商明示 NVMe 或需要 DDoS 防护 → 这单 RackNerd 接不住，看 Sharktech 或 AlphaVPS

下单前最后确认两件事：心仪机房有没有货，以及你打算跑的应用内存门槛是多少。确定之后挑对应档位就行：👉 [查看 RackNerd 全部 VPS 套餐与当前价格](https://bit.ly/RacKnerd)
