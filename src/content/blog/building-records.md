---
title: '个人博客搭建记录'
description: '搭建半自动化平台，在本地完成 MD 文档编写并上传后，自动部署至 Web 端'
pubDate: 'april 11 2025'
heroImage: '../../assets/building-records.jpeg'
---
> 搭建半自动化平台，在本地完成 MD 文档编写并上传后，自动部署至 Web 端
>

## 技术选型
---

+ 前端 Node.js 框架：Astro
+ 代码托管：GitHub
+ 网站自动部署：Vercel

## 开始部署
---

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
此步骤略过。。。

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
### 添加新博客
在`/src/pages/blog/`下拷贝`md`文档，在`src/assets/`下引用图片和字体等元素

### `.astro`文件
1. 编写 Astro 模板非常像编写 HTML，但你可以在其中加入 JavaScript 表达式。
2. Astro 的 frontmatter 脚本只包含 JavaScript。
3. 你可以在你的 .astro 文件的任何部分使用所有现代的 JavaScript 逻辑运算符、表达式和函数。但是，大括号仅在 HTML 模板主体中是必要的。

```html
---
// 此处为frontmatter栏，可以在组件的前面使用脚本标签来定义变量和使用 JavaScript 表达式。
// 导入外部资源
// import '../styles/global.css';

// 定义变量
const pageTitle = "测试页";

// 使用 JS 表达式
const identity = {
    firstName: "莎拉",
    country: "加拿大",
    occupation: "技术撰稿人",
    hobbies: ["摄影", "观鸟", "棒球"],
};

const skills = ["HTML", "CSS", "JavaScript", "React", "Astro", "Writing Docs"];

const happy = true;
const finished = false;
const goal = 3;

const skillColor = "crimson";
---

<html lang="zh-cn">
    <head>
        <meta charset="utf-8" />
        <meta name="viewport" content="width=device-width" />
        <title>{pageTitle}</title>
        
        <!-- 在单页面使用 CSS 样式-->
        <!-- 使用 define:vars={ {...} } 指令引用 frontmatter 中的任何变量 -->
        <style define:vars={{skillColor}}>
            .skill {
                /* 在样式标签中（即此处）用作 CSS 变量使用 */
                color: var(--skillColor);
                font-weight: bold;
            }
        </style>
    </head>
    <body>
        <p>以下是关于我的几个事实：</p>
        <ul>
            <!-- 在 astro 使用 JS 表达式 -->
            <li>我的名字是{identity.firstName}.</li>
            <li>我住在{identity.country}。我的职业是{identity.occupation}。</li>
            {
                identity.hobbies.length >= 2 && (
                    <li>
                        我的两个习惯：{identity.hobbies[0]}和
                        {identity.hobbies[1]}
                    </li>
                )
            }
        </ul>
        {happy && <p>我非常乐意学习 Astro！</p>}

        {finished && <p>我完成了这节教程！</p>}

        {
            // 使用三元表达式 / 条件渲染元素
            goal === 3 ? (
                <p>我的目标是在三天内完成。</p>
            ) : (
                <p>我的目标不是 3 天。</p>
            )
        }
        <p>我的技能：</p>
        <ul>
            {skills.map((skill) => <li class="skill">{skill}</li>)}
        </ul>
    </body>
</html>
```

### todo
+ 跟换字体
+ 优化行间距
+ 代码块和字体过大
