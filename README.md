# 📺 TVBox 影视仓 一键配置说明

> 所有源已经过实测(2026-08-31)，按速度排序，失效自动跳过。

## 方式一：单仓集合（推荐，自动轮询）⭐

把下面**一个链接**填进影视仓的"配置地址"即可：

```
https://raw.githubusercontent.com/Damon-zhouyufeng/tvbox-sources/main/tvbox_multi.json
```

**效果**：客户端自动按顺序尝试 13 个仓源，第一个失效自动用下一个。

## 方式二：直播源集合

直播设置里填这个（自动轮询 14 个直播源）：

```
https://raw.githubusercontent.com/Damon-zhouyufeng/tvbox-sources/main/live_sources.txt
```

## 文件说明

| 文件 | 内容 | 用途 |
|---|---|---|
| `tvbox_multi.json` | 13 个仓源（按速度排序）| 影视点播自动轮询 |
| `live_sources.txt` | 14 个直播源（按速度排序）| 直播自动轮询 |
| `README.md` | 本说明 | — |

## 手动备份（不想用仓库时）

### 单仓备用（任选其一粘贴）
```
http://home.jundie.top:81/top98.json          # 最快0.2s
https://raw.githubusercontent.com/maoystv/6/main/000.json   # 最全78KB
https://raw.githubusercontent.com/gaotianliuyun/gao/master/js.json
```

### 直播备用（任选其一）
```
https://raw.githubusercontent.com/Guovin/iptv-api/gd/output/ipv4/result.m3u   # 473频道
https://raw.githubusercontent.com/suxuang/myIPTV/refs/heads/main/ipv6.m3u     # 862频道, 0.96s
https://3043.kstore.space/bhvip/bhzb.txt                                      # 631频道
```
