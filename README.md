# IPTV 直播源

适用于 TVBox、IPTV 等播放器的直播源收集整理。

## 直播源列表

### 主要直播源

#### TXT 格式（传统格式）

| 文件名 | 说明 | 链接 |
|--------|------|------|
| live.txt | 常规频道（央视、卫视、体育、影视、少儿） | [点击查看](https://raw.githubusercontent.com/lingyu-lk/iptv/main/live.txt) |
| live-4k.txt | 4K/8K超高清频道 | [点击查看](https://raw.githubusercontent.com/lingyu-lk/iptv/main/live-4k.txt) |
| live-gangtai.txt | 港澳台频道 | [点击查看](https://raw.githubusercontent.com/lingyu-lk/iptv/main/live-gangtai.txt) |
| live-18plus.txt | 成人频道（18+） | [点击查看](https://raw.githubusercontent.com/lingyu-lk/iptv/main/live-18plus.txt) |

#### JSON 格式（推荐，TVBox 标准格式）

| 文件名 | 说明 | 链接 |
|--------|------|------|
| live.json | 常规频道（央视、卫视、体育、影视、少儿） | [点击查看](https://raw.githubusercontent.com/lingyu-lk/iptv/main/live.json) |
| live-4k.json | 4K/8K超高清频道 | [点击查看](https://raw.githubusercontent.com/lingyu-lk/iptv/main/live-4k.json) |
| live-gangtai.json | 港澳台频道 | [点击查看](https://raw.githubusercontent.com/lingyu-lk/iptv/main/live-gangtai.json) |
| live-18plus.json | 成人频道（18+） | [点击查看](https://raw.githubusercontent.com/lingyu-lk/iptv/main/live-18plus.json) |

## 使用方法

### TVBox 使用方法

#### 方法一：直接添加直播源（推荐）

1. 复制上面表格中的直播源链接
2. 打开 TVBox 应用
3. 进入 **设置** → **直播设置** → **直播配置地址**
4. 粘贴直播源链接
5. 点击确认保存

#### 方法二：通过配置文件引用

在 TVBox 的主配置文件（JSON格式）中添加：

```json
{
  "sites": [...],
  "lives": [
    {
      "name": "常规频道",
      "type": 0,
      "url": "https://raw.githubusercontent.com/lingyu-lk/iptv/main/live.txt"
    },
    {
      "name": "4K超高清",
      "type": 0,
      "url": "https://raw.githubusercontent.com/lingyu-lk/iptv/main/live-4k.txt"
    },
    {
      "name": "港澳台",
      "type": 0,
      "url": "https://raw.githubusercontent.com/lingyu-lk/iptv/main/live-gangtai.txt"
    },
    {
      "name": "成人频道",
      "type": 0,
      "url": "https://raw.githubusercontent.com/lingyu-lk/iptv/main/live-18plus.txt"
    }
  ]
}
```

### 其他播放器使用

- **VLC播放器**：打开网络串流，输入直播源链接
- **PotPlayer**：文件 → 打开 → 打开链接，输入直播源链接
- **IPTV Smarters**：添加播放列表，使用 M3U URL

## 频道分类

### live.txt 包含：
- 央视频道（CCTV1-17）
- 卫视频道（湖南、浙江、江苏等）
- 体育频道（CCTV5、CCTV5+、广东体育等）
- 影视频道（CHC系列、欢笑剧场等）
- 少儿频道（CCTV14、金鹰卡通等）

### live-4k.txt 包含：
- CCTV 4K/8K
- 纯享4K
- 欢笑剧场4K
- 苏州4K
- 其他4K频道

### live-gangtai.txt 包含：
- 凤凰系列（凤凰中文、凤凰资讯、凤凰香港）
- TVB系列（翡翠台、明珠台）
- 台湾频道（台视、中视、华视、民视等）
- 香港卫视、澳门卫视

### live-18plus.txt 包含：
- 成人频道（需要18岁以上观看）

## 注意事项

1. **网络要求**：
   - 某些直播源需要特定运营商网络（电信、联通、移动组播源）
   - 部分源为内网地址，仅在相应网络环境下可用

2. **IPv6支持**：
   - 部分直播源使用IPv6地址（如 `[2409:8087:...]`）
   - 需要你的网络和设备支持IPv6

3. **链接稳定性**：
   - 直播源地址可能会失效，建议定期更新
   - 如发现失效链接，请提交Issue

4. **播放问题**：
   - 如果某个源无法播放，请尝试列表中的其他源
   - 建议使用支持硬件解码的播放器

## GitHub 加速

如果 GitHub Raw 访问较慢，可以使用以下加速服务：

将 `raw.githubusercontent.com` 替换为：
- `ghproxy.com/https://raw.githubusercontent.com`
- `raw.fastgit.org`

示例：
```
https://ghproxy.com/https://raw.githubusercontent.com/lingyu-lk/iptv/main/live.txt
```

## 更新日志

- 2025-12-25：初始版本，整理分类直播源

## 免责声明

本项目仅供学习交流使用，所有直播源均收集自互联网。请勿用于商业用途。

如有侵权，请联系删除。

## Star History

如果这个项目对你有帮助，请给个 ⭐️ Star 支持一下！

## License

MIT License
