# e-home-party-app

> 党建移动端应用 - 基于 Vue.js 开发的移动端党建管理系统

## 项目简介

本项目是一个面向党员的移动端党建管理应用，提供党建学习、组织生活、党员互动、积分管理等功能，帮助党员随时随地参与党建活动。

## 主要功能

### 📱 核心功能模块

- **通知早知道** - 及时接收党建相关通知公告
- **我的党建** - 个人党建信息中心
- **新闻资讯** - 多栏目新闻浏览
  - 信工新闻眼
  - 党建一点通
  - 党员亮身份
  - 政治学习
  - 随时随地学
  - 制度建设
  - 特色活动
- **组织生活** - 掌上组织生活管理
- **思想汇报** - 提交和查看思想汇报
- **心得总结** - 学习心得总结管理
- **民主评议** - 参与民主评议活动
- **流动党员找组织** - 帮助流动党员找到组织
- **随时随地拍** - 上传党建活动照片
- **党员云互动** - 党员之间的互动交流
- **党史上的今天** - 了解党史重要事件
- **个人量化积分** - 查看和管理个人积分
- **缴纳党费** - 在线缴纳党费
- **个人信息管理** - 个人信息查看和修改

## 技术栈

- **框架**: Vue.js 2.5.2
- **路由**: Vue Router 3.0.1
- **状态管理**: Vuex 3.0.1 + vuex-persistedstate 2.5.4
- **UI组件库**: Mint UI 2.2.13
- **HTTP请求**: Axios 0.18.0
- **轮播组件**: vue-awesome-swiper 2.6.7
- **构建工具**: Webpack 3.12.0
- **样式预处理**: Sass/SCSS
- **其他工具**:
  - qs (数据序列化)
  - cheerio (HTML解析)

## 项目结构

```
e-home-party-app/
├── build/              # Webpack 构建配置
├── config/             # 项目配置文件
├── src/
│   ├── assets/         # 静态资源文件
│   ├── components/     # 公共组件
│   │   ├── com-header.vue    # 头部组件
│   │   ├── tabs.vue          # 底部导航组件
│   │   └── Nullcontent.vue   # 空内容组件
│   ├── router/         # 路由配置
│   ├── store/          # Vuex 状态管理
│   ├── style/          # 样式文件
│   ├── utils/          # 工具函数
│   │   ├── index.js          # 工具函数（axios封装、时间处理等）
│   │   ├── islogin.js        # 登录状态检查
│   │   └── getPartyToday.js  # 党建今日数据
│   ├── views/          # 页面组件
│   ├── App.vue         # 根组件
│   └── main.js         # 入口文件
├── static/             # 静态文件目录
└── index.html          # HTML 模板
```

## 环境要求

- Node.js >= 6.0.0
- npm >= 3.0.0

## 安装与运行

### 安装依赖

```bash
npm install
```

### 开发环境运行

```bash
# 启动开发服务器（默认端口：3007）
npm run dev
# 或
npm start
```

开发服务器将在 `http://192.168.1.160:3007` 启动（可在 `config/index.js` 中配置）

### 生产环境构建

```bash
# 构建生产版本
npm run build

# 构建并查看打包分析报告
npm run build --report
```

构建后的文件将输出到 `dist/` 目录

## 配置说明

### API 代理配置

开发环境的 API 代理配置在 `config/index.js` 中：

```javascript
proxyTable: {
  '/api': {
    target: 'http://211.67.177.56:8080/hhdj',
    changeOrigin: true,
    pathRewrite: {
      '/api': '/'
    }
  }
}
```

### 状态管理

项目使用 Vuex 进行状态管理，并使用 `vuex-persistedstate` 实现状态持久化（存储在 sessionStorage 中）。

主要状态包括：
- `userInfo`: 用户信息
- `token`: 认证令牌
- `interact`: 互动信息

## 主要特性

- ✅ 响应式设计，适配移动端
- ✅ 路由懒加载，优化首屏加载速度
- ✅ 状态持久化，提升用户体验
- ✅ Token 认证机制
- ✅ 统一的 HTTP 请求封装
- ✅ 组件化开发，代码复用性高

## 浏览器支持

- iOS Safari
- Android Chrome
- 微信内置浏览器
- 其他现代移动浏览器

## 开发规范

- 使用 Vue 单文件组件（.vue）进行开发
- 样式使用 SCSS 预处理器
- 遵循 Vue.js 官方风格指南
- 组件命名采用 PascalCase
- 路由配置使用懒加载方式

## 作者

WangShaoqi <924384288@qq.com>

## ☕ 请作者喝杯奶茶

如果这个项目对你有帮助，欢迎请作者喝杯奶茶 🥤

<div align="center">
  <img src="https://raw.githubusercontent.com/RiverGodo/gallery/main/pay.png" alt="请作者喝杯奶茶" width="400">
</div>

---
