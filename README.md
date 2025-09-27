# AutoMovieResourcesManager

## 📖 简介

AutoMovieResourcesManager 是一个强大的全自动媒体资源管理工具，使用网盘strm同步，AI智能刮削及整理，302反代等完成对网盘资源的管理

## ✨ 核心特性

- 🔍 **智能刮削**
  - 采用AI全自动刮削功能
  - 支持TMDB/IMDB/豆瓣
  - 支持网盘手动刮削
  - 支持本地手动刮削

- 📱 **多网盘支持**
  - 支持123网盘、天翼云盘
  - 即将兼容夸克网盘、UC网盘
  - 多网盘，多账号，同类型网盘支持多个账号

- 📱 **自动分类**
  - 支持最多19个分类，包含迪士尼、电视剧、电影、动漫电影、儿童、番剧、高分电视剧、高分电影、国产动漫、国产剧、国内电影、国外电影、韩剧、纪录片、科幻大片、奈飞、欧美剧、日剧、综艺
  - 智能媒体库海报生成

- 📱 **网盘文件自动strm同步**
  - 支持同步网盘的内的strm
  - 支持全自动302反代

- 📱 **Emby使用优化**
  - 优化302反单，多源更快返回

- 🔐 **其他功能**
  - 执行队列状态监控
  - 任务状态监控及手动执行
  - 189网盘全自动签到
  - 更好的189配置方法

## 🖥️ 功能展示

<details>
<summary>📺 媒体库海报</summary>
<div align="center">
    <img src="img/媒体库.png" width="800"/>
    <p>基于豆瓣评分的智能影视推荐</p>
</div>
</details>

<details>
<summary>🔍 前端UI</summary>
<div align="center">
    <img src="img/前端.png" width="800"/>
    <p>前端管理界面</p>
</div>
</details>

## 🚀 快速开始

### 快速入门指南
[快速入门指南](./快速入门手册)

## 预览功能
[快速预览](./页面预览集说明/快速预览功能.md)


### 系统要求
- Docker 运行环境

### Docker 部署
compose见docker-compose.yml文件
注意: 配置前请先配置好如下配置，并放置到config目录下

### 全局配置说明(config.yaml，放在config目录下，需要单独映射)
```yaml
redis:      # redis配置
  prefix_key: "api"   # redis前缀
  is_cluster: false
  host: "xx.xx.xx.xx"   # redis的ip地址
  port: 6379      # redis的端口
  db: 9       # redis的db库
  decode_responses: true
  max_connections: 500

ProxyUrl: "https://xxx.xxxx.xx"     # CloudFlare 的反向代理地址，访问外网时使用

mapper_connection:            # 数据库配置
  engine: tortoise.backends.asyncpg
  credentials:
    host: "xxx.xxxx"    # 数据库ip
    port: 5432        # 数据库端口     
    user: 'test'      
    password: '123456'
    database: 'auto-movie-resources-manager'  # 数据库名

rabbitmq_url: "amqp://admin:admin@xx.xxx.xx:5672/"     # rabbitmq_url数据库配置

notice:       # 通知配置，目前只支持ntfy
  type: "ntfy"
  url: "http://xx.xxx.xxx/auto_video_1"

is_debug: false

strm_url: "https://xx.xx.xx.xx:8090"    # 需要302的strm地址，会写入strm内，如果需要外网访问建议填公网地址

save_file_suffix:     # 附属文件后缀，这些文件会下载到本地
  - nfo
  - srt
  - ass
  - str
  - sub
  - ssa

Emby:
  url: "http://xx.xxx.xx:8096"         # Emby地址
  api_key: "12312312"      # Emby 秘钥
  video_folder: "/video"         # Emby 路径前缀，如果emby内部路径为/video, 本服务路径为/video/123,则填/video

baidu_translate:
  appid: "xxx"        # 百度翻译appid，用于生成媒体库海报图
  secret_key: "xxxx"


```

## 其他配置说明
[Emby 配置说明](./其他/Emby配置说明.md)

[AI平台支持](./其他/AI平台支持.md)

[网盘配置说明](./其他/网盘配置说明.md)

[刮削配置说明](./其他/刮削配置说明.md)


## 版本说明
[版本说明](./版本说明.md)


## 版本说明
[许愿池](./许愿池/许愿池.md)


## 免责申明
AutoMovieResourcesManager 仅用于学习，请勿用于非法用途。禁止任何商业用途。

---
<div align="center">
    <p>Made with ❤️ by AutoMovieResourcesManager Team</p>
</div> 
