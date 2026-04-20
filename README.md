# 个人博客搭建
> 搭建半自动化平台，在本地完成 MD 文档编写并上传后，自动部署至 Web 端

## 技术选型

+ 前端 Node.js 框架：Astro
+ 代码托管：GitHub
+ 网站自动部署：Vercel

## 主要技术栈
+ Astro (v6.1.5)：核心框架，用于静态站点生成和组件化开发
+ @astrojs/mdx：支持在 Markdown 中嵌入组件
+ @astrojs/rss 和 @astrojs/sitemap：自动生成 RSS 订阅和站点地图
+ Sharp：图像优化
+ TypeScript：类型安全配置

## 开始部署

```bash
# 使用 npm 创建
npm create astro@latest -- --template blog
```

### 项目结构
```plain
. (项目根目录)
├── public/                # 📂 纯静态资源目录
│   │                      # 这里的文件不经过编译，直接部署到网站根目录
│   ├── favicon.svg        # 🌐 网站图标
│
├── src/                   # 📂 源代码主目录 (你 90% 的工作都在这里)
│   ├── components/        # 📦 UI 组件库 (复用的零件)
│   │   ├── Header.astro   # 🔝 顶部导航栏
│   │   ├── Footer.astro   # 🔚 底部版权页
│   │   └── Card.astro     # 🎴 卡片式展示组件
│   │
│   ├── layouts/           # 🖼️ 页面布局模板 (公共外壳)
│   │   └── BaseLayout.astro # 基础布局，包含 <html><head> 等
│   │
│   ├── pages/             # 🛣️ 路由与页面 (非常重要！)
│   │   │                  #此目录的文件名直接决定了网站的网址(URL)
│   │   ├── index.astro    # 🏠 网站首页 (yourdomain.com/)
│   │   ├── about.astro    # 📖 "关于"页面 (yourdomain.com/about)
│   │   │
│   │   └── posts/         # ✍️ 【✍️这里是你平时更新博客的地方】
│   │       ├── hello.md   # 第一篇文章 (yourdomain.com/posts/hello)
│   │       └── test.mdx   # MDX文件，可在 Markdown 插入组件
│   │
│   └── styles/            # 🎨 样式目录
│       └── global.css     # 全局 CSS 样式
│
├── astro.config.mjs       # ⚙️ Astro 框架配置文件
├── package.json           # 📋 项目依赖与脚手架命令
├── README.md              # 📖 项目说明文档
└── tsconfig.json          # 🔧 TypeScript 配置文件
```

`src/pages/`目录中的`.astro`或`.md`文件。每个页面都根据其文件名作为路由暴露。

`src/components/`目录中放置`Astro/React/Vue/Svelte/Preact`组件。

`src/content/`目录包含相关 Markdown 和 MDX 文档的“集合”。使用`getCollection()`从`src/content/blog/`获取帖子，并使用可选的 schema 对 frontmatter 进行类型检查。查看 [Astro 的内容集合文档](https://docs.astro.build/en/guides/content-collections/)以了解更多信息。

`public/`目录存放任何静态资源，例如图片。

### 相关命令
所有命令都在项目的根目录下，通过终端运行，更多命令可查看[官方技术文档](https://docs.astro.build/)：

| Command | Action |
| --- | --- |
| `npm install` | Installs dependencies |
| `npm run dev` | Starts local dev server at `localhost:4321` |
| `npm run build` | Build your production site to `./dist/` |
| `npm run preview` | Preview your build locally, before deploying |
| `npm run astro ...` | Run CLI commands like `astro add`<br/>, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI |


### 上传至 GitHub
#### 创建 GitHub 项目仓库
此步骤略过

#### 本地 push 至 GitHub 云端
```bash
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/ username/repository.git
git push -u origin main
```

### 使用 Vercel 自动部署网站
#### 通过网站 UI 部署
1. 将你的代码推送到你的在线 Git 存储库（GitHub、GitLab、BitBucket 等）。
2. [导入你的项目](https://vercel.com/new) 至 Vercel。
3. Vercel 将自动检测 Astro 项目并自动为其配置正确的设置。
4. 你的应用程序已部署完成了！（例如：[astro.vercel.app](https://astro.vercel.app/)）

> 前往 [网站部署](https://docs.astro.build/zh-cn/guides/deploy/vercel/) 页了解详情
>

## 项目优化
请前往[项目搭建记录](./src/content/blog/building-records.md)查看