# 📺 TVBox 影视仓 配置集合

> 最近更新：**2026-10-04**
> 本轮：在原有 387 个频道名基础上，合并 **iptv-org/iptv** 官方公共源 → 658 条 → 归一 387 个频道名（242 个带备用源）→ 逐个实测 → **280 个可播（72%）**，其中 **209 个响应 <2s**

---

## 🚀 方式一：直播源（推荐）

### 免代理直连（GitHub 走加速镜像）

```
https://gh-proxy.com/https://raw.githubusercontent.com/Damon-zhouyufeng/tvbox-sources/main/live_cn.m3u
```

> 备选镜像（择一，均已实测）：
> - `https://fastly.jsdelivr.net/gh/Damon-zhouyufeng/tvbox-sources@main/live_cn.m3u`
> - `https://gcore.jsdelivr.net/gh/Damon-zhouyufeng/tvbox-sources@main/live_cn.m3u`
> - ~~`ghproxy.net`~~ 已失效，勿用

### 原始地址

| 文件 | 频道数 | 说明 |
|---|---|---|
| `live_cn.m3u` | **209** | ⭐ 全部实测 <2s，国内直连流畅，**推荐** |
| `live.m3u` | **280** | 全部本轮实测可用的频道 |

```
https://raw.githubusercontent.com/Damon-zhouyufeng/tvbox-sources/main/live_cn.m3u
https://raw.githubusercontent.com/Damon-zhouyufeng/tvbox-sources/main/live.m3u
```

**频道分组（5 组）**：📺央视(29) · 📡卫视(35) · 🏙️地方台(198) · 🌏CGTN(16) · 🌐CCTV+国际(2)

---

## 🆕 iptv-org 官方公共源（2026-10-04 新增）

[iptv-org/iptv](https://github.com/iptv-org/iptv) 是全球公共电视台的官方免费源索引，**只收录版权方主动公开的免费流，不含付费内容**。它的 `github.io` 地址**国内可直连**（实测 0.7~5.4s），无需镜像。

**可直接填「直播地址」：**

| 列表 | 地址 | 频道数 | 耗时 |
|---|---|---|---|
| 🇨🇳 中国 | `https://iptv-org.github.io/iptv/countries/cn.m3u` | 145 | 0.7s |
| 🎬 电影 | `https://iptv-org.github.io/iptv/categories/movies.m3u` | 782 | 0.8s |
| 📰 新闻 | `https://iptv-org.github.io/iptv/categories/news.m3u` | — | — |
| 🌍 纪录片 | `https://iptv-org.github.io/iptv/categories/documentary.m3u` | 254 | 0.9s |
| 🇺🇸 美国 | `https://iptv-org.github.io/iptv/countries/us.m3u` | 1,451 | 1.6s |
| 🇬🇧 英国 | `https://iptv-org.github.io/iptv/countries/uk.m3u` | 301 | 1.9s |
| 🇩🇪 德国 | `https://iptv-org.github.io/iptv/countries/de.m3u` | 287 | 0.9s |
| 🇫🇷 法国 | `https://iptv-org.github.io/iptv/countries/fr.m3u` | 209 | 0.9s |
| 🇰🇷 韩国 | `https://iptv-org.github.io/iptv/countries/kr.m3u` | 81 | 0.8s |
| 🇯🇵 日本 | `https://iptv-org.github.io/iptv/countries/jp.m3u` | 7 | 0.7s |
| 🌐 全部 | `https://iptv-org.github.io/iptv/index.m3u` | **11,138** | 5.4s |

URL 规律：`countries/<国家码>.m3u` · `categories/<类别>.m3u`

> ⚠️ **别直接加载 index.m3u** —— 11,138 个台是 2.4MB，弱盒子解析要很久才出第一个画面。挑 1~2 个国家或类别即可。
>
> ⚠️ **外语台没有中文字幕**，这是公共源本身的属性，不是配置问题。想看中字剧情片请走正版平台（B站限免、央视影音、腾讯免费库）。

---

## 🚀 方式二：点播接口（单仓集合）

### 国内直连版（8 个国内域名源，免代理加载）

```
https://gh-proxy.com/https://raw.githubusercontent.com/Damon-zhouyufeng/tvbox-sources/main/tvbox_cn.json
```

### 完整版（13 个源，含 GitHub 源）

```
https://gh-proxy.com/https://raw.githubusercontent.com/Damon-zhouyufeng/tvbox-sources/main/tvbox_multi.json
```

### 多仓（可选，客户端可切换多个仓）

```
https://gh-proxy.com/https://raw.githubusercontent.com/Damon-zhouyufeng/tvbox-sources/main/tvbox_duocang.json
```

> ⚠️ **部分盒子不认 JSON 数组多源集合**（会报"接口无效"）。若报错，改用下面的单条源。

---

## 📋 单条源（多源集合报错时用）

### 单仓 · 国内域名（免代理，推荐）

| 源 | 地址 | 速度 | 站点 |
|---|---|---|---|
| 🚀 **动漫城** | `https://www.yingm.cc/dm/dm.json` | 0.1s | 27 |
| 🚀 **菜妮丝** | `https://tv.菜妮丝.top` | 0.8s | ✓ |
| 🚀 **真心** | `https://www.252035.xyz/z/FongMi.json` | 1.0s | ✓ |
| 🚀 **HG** | `https://api.hgyx.vip/hgyx.json` | 1.6s | ✓ |
| 🚀 **摸鱼儿** | `http://我不是.摸鱼儿.com` | 1.7s | ✓ |
| 🚀 **俊佬** | `http://home.jundie.top:81/top98.json` | 0.1~2.3s ⚠️偶发超时 | 24 |
| 小盒子单仓 | `http://xhztv.top/xhz` | 2.5s | ✓ |
| 小盒子4K | `http://xhztv.top/4k.json` | 4.0s | ✓ |

### 单仓 · GitHub 源（内容最全，建议配加速镜像）

| 源 | 地址 | 速度 | 站点 |
|---|---|---|---|
| 🚀 **高天流云** ⭐ | `https://raw.githubusercontent.com/gaotianliuyun/gao/master/js.json` | 0.7s | **298** |
| 🚀 **dxawi** | `https://dxawi.github.io/0/0.json` | 0.7s | 48 |
| 🚀 **宝盒VIP** | `https://raw.githubusercontent.com/guot55/YGBH/main/vip2.json` | 0.8s | ✓ |
| 🚀 **分享** | `https://raw.githubusercontent.com/maoystv/6/main/000.json` | 0.9s | ✓ |
| 🚀 **香雅情** | `https://raw.githubusercontent.com/xyq254245/xyqonlinerule/main/XYQTVBox.json` | 1.8s | ✓ |

### 多仓

| 源 | 地址 | 速度 |
|---|---|---|
| 🚀 游魂多仓 | `https://www.iyouhun.com/tv/dc` | 0.8s |
| 🚀 游魂多仓（备） | `https://www.iyouhun.com/tv/yh` | 0.7s |
| 🚀 小盒子多仓 | `http://xhztv.top/dc/` | 0.7s |
| 🚀 小盒子多仓（备） | `http://xhztv.top/DC.txt` | 1.7s |
| 🚀 拾光多仓 | `http://xmbjm.fh4u.org/dc.txt` | 0.7s |

### 直播源 · 国内直连

| 源 | 地址 | 频道 |
|---|---|---|
| 🚀 zbds-iptv4 | `https://live.zbds.top/tv/iptv4.txt` | 711 |
| 🚀 宝盒直播 | `https://3043.kstore.space/bhvip/bhzb.txt` | 612 |
| 🚀 OTT-B站直播 | `https://sub.ottiptv.cc/bililive.m3u` | 858 |
| 🚀 OTT-YY轮播 | `https://sub.ottiptv.cc/yylunbo.m3u` | 530 |
| 🚀 游魂直播 | `https://www.iyouhun.com/tv/zb` | TXT格式 |

---

## 📁 文件说明

| 文件 | 内容 | 用途 |
|---|---|---|
| `live_cn.m3u` | 209 个 <2s 快速频道 | ⭐ 直播地址（推荐） |
| `live.m3u` | 280 个已验证频道 | 直播地址（全量） |
| `tvbox_cn.json` | 8 个国内域名仓源 | 配置地址（免代理） |
| `tvbox_multi.json` | 13 个仓源 | 配置地址（完整） |
| `tvbox_duocang.json` | 5 个多仓 | 配置地址（多仓） |
| `live_sources_cn.m3u` | 6 条国内直播源清单 | 直播源订阅列表 |
| `live_sources.txt` | 19 条直播源（含需镜像的） | 直播源订阅列表 |
| `README.md` | 本说明 | — |

---

## 📊 2026-10-04 本轮统计

| 阶段 | 数量 |
|---|---|
| 合并输入条目（本仓历史 + iptv-org cn） | 658 |
| 名称归一后频道名 | 387 |
| 其中带备用源的频道 | 242 |
| 逐个试连（每频道最多 4 个备用 URL，取首个连通） | — |
| **实测可播** | **280（存活率 72%）** |
| 其中响应 <2s | **209** |

---

## 🔍 验证方法

- **接口源**：HTTP GET，判定返回体为合法 JSON（含 `sites`/`url`/`name`）或 M3U（`#EXTM3U`/`#EXTINF`）
- **直播频道**：逐个 GET 流地址，判定 `#EXTM3U` 头 / `Content-Type: mpegurl|video` / MPEG-TS 同步字节 `0x47`
- 每频道最多试 **4 个备用 URL**，取第一个连通的
- **测源一律用 `curl --noproxy '*'`** —— 走代理失败只说明代理有问题，不代表源不可达（本机 Clash 上游曾指向过期泰国 IP，导致"全部 HTTP 000"的假故障）

---

## ❌ 历史已失效（勿再用）

`OK影视(内/公开)` · `fty.xxooo.cf` · `毒盒` · `饭太硬` · `肥猫` · `巧记` · `道长` · `哪吒` · `喵影视` · `七星宝盒` · `斗鱼影厅` · `驸马` · `小苹果` · `多多影音` · `潇洒(kstore全部)` · `短剧` · `T4`(451) · `青龙`(423) · `港澳4Gtv` · `王二小放牛娃`(返回非配置) · `小米`(返回HTML)

> 游魂的 `goodiptv.club` 地址已失效，新地址为 `https://sub.ottiptv.cc/xxx.m3u`

---

## ⚠️ 使用提示

1. **GitHub 地址务必加加速镜像**（本 README 已给出），否则国内加载可能超时
2. **免费直播源寿命短**（几天到几周），频道失效时重新拉取本仓库即可
3. **加载了频道列表 ≠ 能播放**：黑屏有声 = 解码器问题（切 Exo→Ijk/VLC/MXPlayer）；一直转圈 = 到流服务器网络问题
4. 部分盒子对 JSON 数组多源集合不兼容，报"接口无效"时改用单条源
