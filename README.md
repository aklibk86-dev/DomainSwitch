# DomainSwitch - 智能域名跳转系统

![智能域名跳转系统](https://img.shields.io/badge/Version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Telegram](https://img.shields.io/badge/Telegram-Group-blue.svg)

## 🌟 项目简介

DomainSwitch 是一个现代化的智能域名跳转系统，专门设计用于多域名环境下的智能路由和负载均衡。系统通过实时测速技术自动选择最快的可用域名，提供流畅的用户体验和优雅的界面设计。

## ✨ 核心特性

### 🚀 智能测速路由
- **实时域名测速**: 使用先进的 Image 对象测速技术，避免 CORS 问题
- **并行测试**: 同时测试所有域名，快速确定最优路径
- **智能备选**: 当所有域名测速失败时，自动使用备用域名

### 🎨 精美主题系统
- **多主题支持**: 内置 6+ 精美主题（默认、暗黑、温暖、深海蓝、日落橙、森林绿、紫罗兰、樱花粉）
- **毛玻璃效果**: 现代化毛玻璃设计，支持背景模糊效果
- **响应式设计**: 完美适配桌面和移动设备

### ⚡ 用户体验优化
- **倒计时跳转**: 5秒倒计时，提供取消选项
- **浏览器检测**: 自动识别微信/QQ浏览器，提供引导提示
- **粒子动画**: 优雅的背景粒子动画效果
- **进度条**: 可视化跳转进度指示

### 🔧 高度可配置
- **灵活配置**: 通过 [`js/config.js`](js/config.js:1) 轻松配置域名、主题和参数
- **模块化设计**: 易于扩展和维护的代码结构
- **详细注释**: 完整的代码注释和文档

## 🎯 使用场景

- **多CDN优化**: 自动选择最快的CDN节点
- **域名切换**: 主域名故障时自动切换到镜像站点
- **负载均衡**: 在多服务器间智能分配流量
- **用户体验**: 提供专业的跳转页面和状态反馈

```
DomainSwitch/
├── index.html              # 主页面
├── popup.html             # 弹窗页面
├── css/                   # 样式文件
│   ├── base.css           # 基础样式
│   ├── themes.css         # 主题样式
│   ├── responsive.css     # 响应式样式
│   ├── particles.css      # 粒子效果
│   └── popup.css          # 弹窗样式
├── js/                    # JavaScript文件
│   ├── config.js          # 配置文件
│   ├── main.js            # 主逻辑
│   ├── browser-detect.js  # 浏览器检测
│   ├── domain-speed.js    # 域名测速
│   ├── countdown.js       # 倒计时功能
│   ├── particles.js       # 粒子效果
│   ├── clipboard.js       # 剪贴板功能
│   └── popup.js           # 弹窗逻辑
└── README.md             # 项目说明
```

## 🚀 快速开始

### 部署方式

#### 方式一：直接部署（推荐）
1. 下载项目文件到您的服务器
2. 修改 [`js/config.js`](js/config.js:18) 中的域名配置
3. 上传到Web服务器即可使用

#### 方式二：CDN部署
1. 将项目上传到CDN服务
2. 配置CORS策略允许图片加载
3. 更新配置文件中的域名列表

#### 方式三：本地测试
1. 使用本地服务器（如Live Server、http-server）
2. 打开 `index.html` 进行测试

### 配置说明

编辑 [`js/config.js`](js/config.js:11) 文件进行自定义配置：

```javascript
const config = {
    domains: [
        {name: "主域名", url: "https://your-domain.com"},
        {name: "镜像一", url: "https://mirror1.com"},
        // 添加更多域名...
    ],
    defaultCountdown: 5,      // 倒计时秒数
    testImagePath: "/favicon.ico", // 测速图片路径
    defaultTheme: "warm"      // 默认主题
};
```

## 🎨 主题预览

系统内置多种精美主题，以下是部分主题效果预览：

![蓝色主题预览](img/蓝色.jpg)
*蓝色主题 - 清新蓝色系*

![橙色主题预览](img/橙色.jpg)
*橙色主题 - 活力橙色系*

![紫色主题预览](img/紫色.jpg)
*紫色主题 - 梦幻紫色系*

其他可用主题：
- **默认主题**: 清新蓝色系
- **暗黑主题**: 深色紫色系
- **温暖主题**: 活力橙色系
- **深海蓝**: 渐变蓝绿色
- **日落橙**: 温暖橙粉色
- **森林绿**: 自然绿色系
- **紫罗兰**: 梦幻紫色系
- **樱花粉**: 柔和粉色系

## 📱 浏览器兼容性

- ✅ Chrome 60+
- ✅ Firefox 55+
- ✅ Safari 12+
- ✅ Edge 79+
- ⚠️ 微信/QQ浏览器（显示引导提示）
- ⚠️ IE 11（部分功能受限）

## 🔧 开发指南

### 添加新主题
1. 在 [`css/themes.css`](css/themes.css:1) 中添加主题样式
2. 在 [`js/config.js`](js/config.js:50) 的 themes 数组中配置颜色变量
3. 设置为主题选择器添加选项

### 自定义测速逻辑
修改 [`index.html`](index.html:94) 中的 `testDomainSpeed` 函数来实现自定义测速算法。

### 扩展功能
项目采用模块化设计，可以轻松添加：
- 地理位置路由
- 用户行为分析
- 性能监控
- A/B测试功能

## 🤝 社区支持

**Telegram 群组**: [https://t.me/htpnu](https://t.me/htpnu)

加入我们的Telegram群组获取：
- 🆘 技术支持与问题解答
- 💡 功能建议与反馈
- 🔄 最新更新通知
- 👥 开发者交流社区

## 📄 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情。

## 🐛 问题反馈

如果您遇到任何问题或有功能建议，请：
1. 检查 [FAQ](#) 部分
2. 在 GitHub 提交 Issue
3. 加入 Telegram 群组寻求帮助

## 🌟 更新日志

### v1.0.0 (2024-09-02)
- ✅ 初始版本发布
- ✅ 智能域名测速功能
- ✅ 多主题支持系统
- ✅ 响应式设计
- ✅ 浏览器环境检测
- ✅ 粒子动画效果

---

**感谢使用 DomainSwitch！** 🚀

如果这个项目对您有帮助，请给个 ⭐ Star 支持我们！
