# 项目说明

## 项目内容

这是一个以湖面、水波、游鱼和昼夜场景为视觉主题的个人作品集，包含同一套桌面版与移动版页面，以及一个复用 Android 音乐库接口的网页版播放器。

## 主要文件

- `Chase-the-light.html`：响应式作品集页面。精选作品中的「湖畔播放器 · Web」必须直接链接到 `web-player.html`，并在新标签页打开。
- `Chase-the-light-desktop.html`：桌面版作品集。作品内容或入口变更时，与主作品集同步。
- `web-player.html`：网页版播放器界面及湖面背景。页面引用 `web-player.js`。
- `web-player.js`：播放器交互，包括在线搜索和播放、歌词与封面、收藏、歌单、播放队列、本地音乐、离线缓存、随机和循环播放、定时停止等。
- `scripts/player-server.cjs`：静态页面服务和音乐库 API 代理。在线接口请求由此服务转发，浏览器端通过同源 `/api/music`、`/api/download` 路由访问。
- `downloads/player.apk`：Android 安装包下载文件。
- `water-selected-clip.wav`：播放器的湖水声试听片段。
- `koi-and-turtles.png`、`lake-smooth-pebbles.png`：湖景背景使用的图像素材。

## 启动与开发

在项目根目录运行：

```sh
node scripts/player-server.cjs
```

然后打开 `http://127.0.0.1:8765/Chase-the-light.html` 查看作品集，或打开 `http://127.0.0.1:8765/web-player.html` 查看播放器。需要保持 Node 服务运行；播放器在线搜索和在线曲目播放依赖 `http://yinyueku.cn/api.php` 接口。

## 修改约定

- 保留单文件 HTML 中现有的 Three.js 湖面背景、昼夜切换、水波交互和响应式样式。
- 修改播放器时同时检查 `web-player.html` 与 `web-player.js`，不要把音乐库请求改成绕过本地代理的跨域浏览器请求。
- 修改精选作品或播放器介绍时，同步桌面版和响应式版；播放器项目入口始终指向当前的 `web-player.html`。
- 本地音乐和离线文件使用浏览器 IndexedDB 缓存；歌单、收藏、最近播放及在线队列使用浏览器本地存储。不要把本地文件上传到音乐库服务。
- 页面路由与素材路径使用相对路径，确保在本地静态服务或同源托管环境中可访问。
- 这是静态页面加一个轻量 Node 服务的项目，没有前端构建步骤或 npm 依赖清单。保持改动简单，避免引入不必要的框架和依赖。
