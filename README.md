# 二蛋工具集 - 纯前端开发者在线工具箱

> 
> 零部署、无后端、全本地运算的开发者实用工具集合，打开即用，所有数据不经过任何服务器。
> https://seawind737.github.io/toolkit/

---

## ✨ 核心特性

| 特性 | 说明 |
| --- | --- |
| **纯静态部署** | 单页HTML+CSS+JS，无需Node构建、无需后端服务，双击即可打开使用 |
| **隐私安全** | 所有编解码、压缩、加密、图片处理全部在浏览器本地完成，不上传任何用户数据 |
| **自适应主题** | 内置深色/浅色双主题，自动记忆用户偏好，全站风格统一 |
| **响应式布局** | 适配PC/平板/移动端，三级下拉导航，移动端折叠菜单 |
| **易扩展** | 统一菜单配置数组，新增工具仅需添加一行配置即可接入导航和首页推荐 |
| **零成本托管** | 可直接部署到 Nginx、GitHub Pages、Cloudflare Pages 任意静态托管平台 |

---

## 🛠️ 工具清单

### 🔧 开发工具

| 工具名称 | 文件路径 | 功能说明 |
| --- | --- | --- |
| JSON 工具 | `./dev/code/json.html` | JSON 格式化、压缩、校验、树形展示、JSONPath 查询 |
| Base64 编解码 | `./dev/code/base64.html` | 文本/图片 Base64、Base64Url 双向转换 |
| MD5 哈希 | `./dev/code/md5.html` | 文本 MD5 摘要计算 |
| SHA 哈希 | `./dev/code/sha.html` | SHA-1 / SHA-256 / SHA-512 多算法哈希计算 |
| JWT 工具 | `./dev/code/jwt.html` | JWT Token 解析、生成、签名校验 |
| URL 编解码 | `./dev/code/url.html` | URL 编码/解码、中文转义处理 |
| 时间戳转换 | `./time/timestamp.html` | 时间戳与常见日期格式互转，支持毫秒/秒级切换 |
| WebSocket 调试 | `./network/ws.html` | WebSocket 客户端在线调试、消息收发测试 |

### 📝 文本处理工具

| 工具名称 | 文件路径 | 功能说明 |
| --- | --- | --- |
| 大小写转换 | `./text/case.html` | 全大写/全小写/首字母大写/小驼峰/下划线命名互转 |
| 随机密码生成 | `./text/pwd.html` | 自定义长度、字符集组合，滑块+输入框联动，密码强度提示 |
| 文本压缩解压 | `./text/compress.html` | 基于 gzip/deflate 的文本压缩/解压，输出 Base64 格式 |
| 文本去重 | `./text/unique.html` | 按行去重，支持忽略大小写、自动去除首尾空格 |
| 正则测试 | `./text/regex.html` | 正则表达式在线匹配、替换，支持 g/i/m 标志位 |

### 🖼️ 图片媒体工具

| 工具名称 | 文件路径 | 功能说明 |
| --- | --- | --- |
| 图片批量压缩 | `./media/image/compress.html` | 支持多图拖拽/粘贴上传、自定义压缩质量/输出格式、自定义文件名后缀、前后对比预览、选中项 ZIP 打包下载/逐个下载 |
| 颜色转换 | `./media/image/color.html` | HEX/RGB/HSL 颜色格式互转，内置拾色器，实时预览色值 |

### 📦 其他实用工具

| 工具名称 | 文件路径 | 功能说明 |
| --- | --- | --- |
| 二维码工具 | `./other/qrcode.html` | 支持自定义尺寸/边距/颜色/纠错等级/中心 Logo 的二维码生成，同时支持图片上传解析二维码内容 |

### 🎮 休闲小游戏

| 游戏名称 | 文件路径 | 功能说明 |
| --- | --- | --- |
| 扫雷 | `./game/mine.html` | 内置初级/中级/高级预设难度，支持自定义行列数/地雷数量，计时器、插旗标记、递归展开空白格 |

---

## 🚀 快速开始

### 本地使用

直接双击根目录 `index.html` 即可在浏览器中打开使用。

### 部署上线

将整个项目目录上传至任意静态文件服务器即可，无需任何环境配置：

```
# 本地启动临时服务（可选）
npx serve .
# 或使用 python
python3 -m http.server 8080
```

---

## 📂 目录结构

```
├── index.html                 # 首页入口，包含导航菜单配置
├── dev/
│   └── code/                 # 编码哈希类工具
│       ├── base64.html
│       ├── md5.html
│       ├── sha.html
│       ├── jwt.html
│       └── url.html
├── time/
│   └── timestamp.html         # 时间戳工具
├── network/
│   └── ws.html                # WebSocket 调试
├── text/
│   ├── case.html              # 大小写转换
│   ├── pwd.html               # 随机密码
│   ├── compress.html          # 文本gzip压缩
│   ├── unique.html             # 文本去重
│   └── regex.html              # 正则测试
├── media/
│   └── image/
│       ├── compress.html      # 图片批量压缩
│       └── color.html         # 颜色转换
├── other/
│   └── qrcode.html            # 二维码工具
└── game/
    └── mine.html              # 扫雷游戏
```

---

## 🎨 自定义扩展

所有菜单配置集中在 `index.html` 中的 `appList` 数组，新增工具仅需在对应分组下添加配置项即可：

```
{
  name: '工具名称',        // 导航显示名
  url: './path/to.html',   // 工具页面路径
  icon: 'fa-code',         // Font Awesome 图标类名
  desc: '工具简述',         // 首页卡片副标题
  homeRecommend: true      // true=首页卡片展示，false=仅在导航菜单显示
}
```

> 
> 分组信息（分组名、图标、主题色）配置在父级节点上，新增子工具无需额外配置分组样式。

---

## 🧰 技术栈

- 基础：原生 HTML5 / CSS3 / JavaScript (ES6+)
- 样式：Tailwind CSS 3 (CDN 引入)
- 图标：Font Awesome 6.4
- 第三方依赖（全部CDN引入）：
  - `pako`：gzip/deflate 文本压缩
  - `qrcode.js` / `jsQR`：二维码生成与解析
  - `jszip`：批量图片 ZIP 打包下载

---

## ⚠️ 注意事项

1. 所有工具均在浏览器本地完成计算，不会上传任何用户输入的敏感数据；
2. 首次打开需要联网加载 CDN 样式与脚本资源；
3. 批量下载图片时，浏览器可能弹出"允许此站点下载多个文件"提示，选择允许即可；
4. 扫雷游戏中**鼠标右键**为插旗标记操作，已阻止浏览器原生右键菜单弹出。

---

悟已往之不谏，知来者之可追

© 2026 二蛋工具集

```