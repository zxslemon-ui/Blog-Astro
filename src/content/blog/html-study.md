---
title: 'HTML 语法学习'
description: '学习 HTML 基础语法'
pubDate: 'april 21 2026'
heroImage: '../../assets/html-study.jpeg'
---
## HTML简介
## HTML基础语法
### HTML 元素的剖析
+ 元素：`<p></p>`
+ 开始标签：`<p>`
+ 内容：`content`
+ 结束标签：`</p>`

### 属性
一个属性应该有：
+ 一个在它和元素名之间的空格。（对于拥有多个属性的元素，属性之间也应该用空格分隔。）
+ 属性名，后跟一个等号。
+ 一个属性值，用开始和结束的引号包裹。

为元素添加属性

```html
<img src="url" alt="图像文本描述" width="300" height="300">
```

布尔属性

当一个布尔属性没有值，或有任何值（甚至像 `"false"`）时，该布尔属性总是被设置为 true。否则，如果该属性没有写在 HTML 标签中，该属性就被设置为 false。

```html
<!-- 使用 disabled 属性来防止终端用户输入文本到输入框中 -->
<input type="text" disabled="disabled" />

<!-- 也可以这样写 -->
<input type="text" disabled />


<!-- 下面这个输入框不包含 disabled 属性，所以用户可以向其中输入 -->
<input type="text" />
```

### 剖析 HTML 文档
```html
<!doctype html>
<html lang="zh-CN">
  <head>
    <meta charset="utf-8" />
    <title>我的测试页面</title>
  </head>
  <body>
    <p>这是我的页面</p>
  </body>
</html>
```

其中包括：

1. `<!doctype html>`：文档类型声明（doctype）。在 HTML 早期（1991-1992 年），doctype 旨在作为一套规则的链接，HTML 页面必须遵循这些规则才能被认为是好的 HTML。doctype 成为了一个历史遗留物，为了让其他一切正常工作而必须包含它。
2. `<html></html>`：`<html>`元素。这个元素包裹了页面上的所有内容。它有时被称为根元素。
3. `<head></head>`：[<head>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/head) 元素。这个元素充当一个容器，用于存放你想包含在 HTML 页面中但不向页面浏览者显示的内容。这包括会出现在搜索结果中的关键字和页面描述、用于样式化内容的 CSS、字符集声明等等。
4. `<meta charset="utf-8">`：[<meta>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/meta) 元素。这个元素代表了不能由其他 HTML 元相关元素（如 [<base>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/base)、[<link>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/link)、[<script>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/script)、[<style>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/style) 或 [<title>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/title)）表示的元数据。[charset](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/meta#charset) 属性将你的文档的字符编码指定为 UTF-8，它包含了绝大多数人类书面语言的字符。通过这个设置，页面现在可以处理它可能包含的任何文本内容。没有理由不设置它，而且它可以帮助避免以后的一些问题。
5. `<title></title>`：[<title>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/title) 元素。它设置了页面的标题，这个标题会出现在加载该页面的浏览器标签页中。当页面被收藏为书签时，页面标题也用于描述该页面。
6. `<body></body>`：[<body>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/body) 元素。它包含了在页面上显示的所有内容，包括文本、图像、视频、游戏、可播放的音轨或其他任何东西。

### 字符引用
在 HTML 中，字符 `<`、`>`、`"`、`'` 和 `&` 是特殊字符。它们是 HTML 语法本身的一部分。

要想在页面给显示这些字符，你需要使用[字符引用](https://developer.mozilla.org/zh-CN/docs/Glossary/Character_reference)。这些是代表字符的特殊代码，用于在这些确切的情况下使用。每个字符引用都以一个与号（&）开始，并以一个分号（;）结束。

| 字面字符 | 字符引用等效项 |
| --- | --- |
| < | `&lt;` |
| > | `&gt;` |
| " | `&quot;` |
| ' | `&apos;` |
| & | `&amp;` |


### HTML 注释
编写 HTML 注释，请将其包裹在特殊标记 `<!--` 和 `-->` 中。

```html
<p>我不在注释里</p>

<!-- <p>但我在注释里</p> -->
```

## HTML 元信息 —— <head> 标签
在页面加载完成的时候，HTML 文档中的[头部](https://developer.mozilla.org/zh-CN/docs/Glossary/Head)是不会显示在 web 浏览器的。它包含了诸如页面的 [<title>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/title)（标题）、指向 [CSS](https://developer.mozilla.org/zh-CN/docs/Glossary/CSS) 的链接（如果你选择用 CSS 来为 HTML 内容添加样式）、指向自定义网页图标的链接和其他的元数据（描述 HTML 的数据，比如作者和描述文档的重要关键词）等信息。Web 浏览器将使用文档[头部](https://developer.mozilla.org/zh-CN/docs/Glossary/Head)的信息正确渲染 HTML 文档。

### 标题
<title>标题</title>

### 元数据
元数据就是描述数据的数据，而 HTML 有一个“官方的”方式来为一个文档添加元数据——[<meta>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/meta) 元素。

许多 `<meta>` 元素包含了 `name` 和 `content` 属性：

+ `name` 指定了 meta 元素的类型；说明该元素包含了什么类型的信息。
+ `content` 指定了实际的元数据内容。

```html
<meta charset="utf-8" />

<!-- 示例 -->
<meta name="author" content="Chris Mills" />
<meta
  name="description"
  content="The MDN Web Docs Learning Area aims to provide
complete beginners to the Web with all they need to know to get
started with developing web sites and applications." />
```

### 为站点增加自定义图标
1. 将其保存在与网站的索引页面相同的目录中，以 `.ico` 格式保存（大多数浏览器支持更通用的格式，如 `.gif` 或 `.png`）
2. 将以下行添加到 HTML 的 [<head>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/head) 块中以引用它：

```html
<link rel="icon" href="favicon.ico" type="image/x-icon" />
```

### 在 HTML 中应用 CSS 和 JavaScript
如今，几乎你使用的所有网站都会使用 [CSS](https://developer.mozilla.org/zh-CN/docs/Glossary/CSS) 来让网页更加炫酷，并使用 [JavaScript](https://developer.mozilla.org/zh-CN/docs/Glossary/JavaScript) 来让网页有交互功能，比如视频播放器、地图、游戏以及更多功能。这些应用在网页中很常见，它们分别使用 [<link>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/link) 元素以及 [<script>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/script) 元素。

+ [<link>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/link) 元素经常位于文档的头部，它有 2 个属性，`rel="stylesheet"` 表明这是文档的样式表，而 `href` 包含了样式表文件的路径：

```html
<link rel="stylesheet" href="my-css-file.css" />
```

+ [<script>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/script) 元素也应当放在文档的头部，并包含 `src` 属性来指向需要加载的 JavaScript 文件路径，同时最好加上 `defer` 以告诉浏览器在解析完成 HTML 后再加载 JavaScript。这样可以确保在加载脚本之前浏览器已经解析了所有的 HTML 内容。这样你就不会因为 JavaScript 试图访问页面上不存在的 HTML 元素而产生错误。实际上有很多方法来处理在你的页面上加载 JavaScript，但对于现代浏览器来说，这是最可靠的方法（对于其他方法，请阅读[脚本加载策略](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Scripting/What_is_JavaScript#%E8%84%9A%E6%9C%AC%E8%B0%83%E7%94%A8%E7%AD%96%E7%95%A5)）。

```html
<script src="my-js-file.js" defer></script>
```

### 为文档设定主语言
最后，值得一提的是可以（而且有必要）为站点设定语言，这个可以通过添加 [lang 属性](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Global_attributes/lang)到 HTML 开始的标签中来实现（就像 [meta-example.html](https://github.com/mdn/learning-area/blob/main/html/introduction-to-html/the-html-head/meta-example.html) 那样），如下所示：

```html
<html lang="zh-CN">
  …
</html>
```

## HTML 的标题与段落
### 实现结构层级
举个例子，在一个故事中，`<h1>` 表示故事的标题，`<h2>` 表示每个章节的标题，`<h3>` 表示每个章节下的子标题，以此类推。

```html
<h1>三国演义</h1>

<p>罗贯中</p>

<h2>第一回 宴桃园豪杰三结义 斩黄巾英雄首立功</h2>

<p>
  话说天下大势，分久必合，合久必分。周末七国分争，并入于秦。及秦灭之后，楚、汉分争，又并入于汉……
</p>

<h2>第二回 张翼德怒鞭督邮 何国舅谋诛宦竖</h2>

<p>
  且说董卓字仲颖，陇西临洮人也，官拜河东太守，自来骄傲。当日怠慢了玄德，张飞性发，便欲杀之……
</p>

<h3>却说张飞</h3>

<p>
  却说张飞饮了数杯闷酒，乘马从馆驿前过，见五六十个老人，皆在门前痛哭。飞问其故，众老人答曰：“督邮逼勒县吏，欲害刘公；我等皆来苦告，不得放入，反遭把门人赶打！”……
</p>
```

### 列表
无序列表

```html
<ul>
  <li>豆浆</li>
  <li>油条</li>
  <li>豆汁</li>
  <li>焦圈</li>
</ul>
```

有序列表

```html
<ol>
  <li>沿这条路走到头</li>
  <li>右转</li>
  <li>直行穿过第一个十字路口</li>
  <li>在第三个十字路口处左转</li>
  <li>继续走 300 米，学校就在你的右手边</li>
</ol>
```

## 构建文档
### HTML 文档基本组成部分
+ 页眉：[<header>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/header)。
+ 导航栏：[<nav>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/nav)。
+ 主内容：[<main>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/main)。主内容中还可以有各种子内容区段，可用 [<article>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/article)、[<section>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/section) 和 [<div>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/div) 等元素表示。
+ 侧边栏：[<aside>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/aside)。经常放置在 [<main>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/main) 中。
+ 页脚：[<footer>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/footer)。

```html
<!doctype html>
<html lang="zh-CN">
  <head>
    <meta charset="utf-8" />
    <title>我的页面标题</title>
    <link
      href="https://fonts.googleapis.com/css?family=Open+Sans+Condensed:300|Sonsie+One"
      rel="stylesheet" />
    <link rel="stylesheet" href="style.css" />
  </head>

  <body>
    <!-- 本站所有网页的统一主标题 -->
    <header>
      <h1>页眉</h1>
    </header>

    <nav>
      <ul>
        <li><a href="#">主页</a></li>
        <li><a href="#">我们的团队</a></li>
        <li><a href="#">项目</a></li>
        <li><a href="#">联系方式</a></li>
      </ul>

      <!-- 搜索栏是站点内导航的一个非线性的方式。 -->

      <form>
        <input type="search" name="q" placeholder="要搜索的内容" />
        <input type="submit" value="搜索" />
      </form>
    </nav>

    <!-- 网页主体内容 -->
    <main>
      <!-- 一篇文章 -->
      <article>
        <h2>文章标题</h2>

        <p>
          但我得向你解释，所有这些谴责快乐和颂扬痛苦的错误观念是如何产生的。为此，我会向你一五一十地说明这一体系，并阐述伟大的真理探索者、人类幸福的杰出建设者的真实教义。
        </p>

        <section>
          <h3>子章节</h3>

          <p>
            没有人因为快乐是快乐而拒绝、厌恶或回避快乐本身，而是因为不知道如何理性地追求快乐的人会遭遇极其痛苦的后果。也没有人因痛苦是痛苦而喜欢或追求或渴望获得痛苦本身，但也偶有辛劳和痛苦能带来极大的快乐的情景。
          </p>

          <p>
            举个微不足道的例子，若不是从中获得好处，我们当中有谁会进行艰苦的体育锻炼？但是，倘若没有恼人的后果，谁有权利指责选择享受快乐的人呢？或者倘若得不到相应快乐，谁能谴责选择避免痛苦的人呢？
          </p>
        </section>

        <section>
          <h3>另外一个子章节</h3>

          <p>
            另一方面，我们以正义的愤慨谴责并厌恶那些被及时行乐迷惑得萎靡不振，被欲望蒙蔽得看不见大难临头的人；因意志软弱而不能履行职责的人，也应受到同样的谴责，这无异于在辛劳和痛苦前退缩。这些情况非常简单且容易区分。闲暇时，当我们的选择权不受限制，当没有什么可以阻止我们做自己最喜欢的事情时，任何快乐都应该受到欢迎，任何痛苦都应该避免。但是在某些情况下，由于责任或商业义务的要求，不时会有不得不拒绝享乐而接受烦恼的情况。
          </p>

          <p>
            因此，智者在这些事情上总是坚持选择的原则：拒绝快乐以获得更大的快乐，或者忍受痛苦以避免更重的痛苦。
          </p>
        </section>
      </article>

      <!-- 辅助内容也可以嵌套在主要内容中 -->
      <aside>
        <h2>相关内容</h2>

        <ul>
          <li><a href="#">哦，我喜欢海边</a></li>
          <li><a href="#">哦，我也喜欢海边</a></li>
          <li><a href="#">尽管在英格兰北部</a></li>
          <li><a href="#">也永远不会停止下雨</a></li>
          <li><a href="#">哦，好吧……</a></li>
        </ul>
      </aside>
    </main>

    <!-- 本站所有网页的统一页脚 -->

    <footer>
      <p>© 2050 某某保留所有权利</p>
    </footer>
  </body>
</html>
```

### 无语义包装器
有时候你可能只想将一组元素组合在一起，用 [CSS](https://developer.mozilla.org/zh-CN/docs/Glossary/CSS) 或 [JavaScript](https://developer.mozilla.org/zh-CN/docs/Glossary/JavaScript) 将它们作为一个整体加以影响。为了应对这种情况，HTML 提供了 [<div>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/div) 和 [<span>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/span) 元素。应配合使用 [class](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Global_attributes#class) 属性提供一些标签，使这些元素能易于定位。

[<span>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/span) 是一个行级无语义元素，最好只用于无法找到更好的语义元素来包含内容时，或者不想增加特定的含义时。例如：

```html
<p>
  国王喝得酩酊大醉，在凌晨 1 点时才回到自己的房间，踉跄地走过门口。<span
    class="editor-note"
    >[编辑批注：此刻舞台灯光应变暗]</span
  >。
</p>
```

[<div>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/div) 是一个块级无语义元素，应仅用于找不到更好的块级元素时，或者不想增加特定的意义时。例如，一个电子商务网站页面上有一个一直显示的购物车组件。

```html
<div class="shopping-cart">
  <h2>购物车</h2>
  <ul>
    <li>
      <p>
        <a href=""><strong>银耳环</strong></a
        >：$99.95
      </p>
      <img src="../products/3333-0985/" alt="银耳环" />
    </li>
    <li>……</li>
  </ul>
  <p>总消费：$237.89</p>
</div>
```

### 换行与水平分割线
<br>：换行元素

<hr>：主题性中断元素

### 网站基本内容
请记录这些对所有页面都通用的内容，例如：

+ 页眉
    - 标题和徽标
    - 站点语言选择器
+ 导航栏
+ 页脚
    - 版权声明
    - 至条款、联系方式和无障碍政策的链接

## 超链接
通过将文本或其他内容包裹在 [<a>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/a) 元素内，并给它一个包含网址的 [href](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/a#href) 属性（也称为超文本引用或目标，它将包含一个网址）来创建一个基本链接。

```html
<p>
  我创建了一个指向
  <a href="https://www.mozilla.org/zh-CN/">Mozilla 主页</a>的链接。
</p>

<!-- 块级链接 -->
<a href="https://developer.mozilla.org/zh-CN/">
  <h1>MDN Web 文档</h1>
</a>
<p>自从 2005 年起，就开始记载包括 CSS、HTML、JavaScript 等网络技术。</p>

<!-- 图片链接 -->
<a href="https://developer.mozilla.org/zh-CN/">
  <img src="mdn_logo.svg" alt="MDN Web 文档" />
</a>
```

用 title 属性 添加支持信息

```html
<p>
  我创建了一个指向
  <a
    href="https://www.mozilla.org/zh-CN/"
    title="了解 Mozilla 使命以及如何参与贡献的最佳站点。">
    Mozilla 主页</a
  >的超链接。
</p>
```

### 统一资源定位符（URL）与路径（path）快速入门
统一资源定位符（Uniform Resource Locator，URL）是一个定义了在网络上的位置的一个文本字符串。例如，Mozilla 的简体中文主页位于 `https://www.mozilla.org/zh-CN/`。

### 文档片段
超链接除了可以链接到文档外，也可以链接到 HTML 文档的特定部分（被称为文档片段）。要做到这一点，你必须首先给要链接到的元素分配一个 [id](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Global_attributes#id) 属性。通常情况下，链接到一个特定的标题是有意义的，这看起来就像下面这样：

```html
<h2 id="Mailing_address">邮寄地址</h2>
```

为了链接到那个特定的 `id`，要将它放在 URL 的末尾，并在前面包含井号（`#`），例如：

```html
<p>
  要提供意见和建议，请将信件邮寄至<a href="contacts.html#Mailing_address"
  >我们的地址</a
  >。
</p>
```

你甚至可以在同一份文档下，通过链接文档片段，来链接到当前文档的另一部分：

```html
<p>本页面底部可以找到<a href="#Mailing_address">公司邮寄地址</a>。</p>
```

绝对 URL 和相对 URL

### 链接到非 HTML 资源——留下清晰的指示
当链接到一个需要下载的资源（如 PDF 或 Word 文档）或流媒体（如视频或音频）或有另一个潜在的意想不到的效果（打开一个弹出窗口），你应该添加明确的措辞，以减少混乱。

```html
<p>
  <a href="https://www.example.com/large-report.pdf">
    下载销售报告（PDF，大小为 10 MB）
  </a>
</p>

<p>
  <a href="https://www.example.com/video-stream/" target="_blank">
    观看视频（将在新标签页中播放，HD 画质）
  </a>
</p>
```

### 在下载链接时使用 download 属性
当你链接到要下载的资源而不是在浏览器中打开时，你可以使用 `download` 属性来提供一个默认的保存文件名。

```html
<a
  href="https://download.mozilla.org/?product=firefox-latest-ssl&os=win64&lang=zh-CN"
  download="firefox-latest-64bit-installer.exe">
  下载最新的 Firefox 中文版 - Windows（64 位）
</a>
```

### 电子邮件链接
当点击一个链接或按钮时，可能会开启新的邮件的发送而不是连接到一个资源或页面。这种场景可以使用 [<a>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/a) 元素和 `mailto:` URL 协议实现。

其最基本和最常用的使用形式为一个指明收件人电子邮件地址的 `mailto:` 链接。例如：

```html
<a href="mailto:nowhere@mozilla.org">向 nowhere 发邮件</a>
```

## HTML 中的图片
如果图像在名为 `images` 的子目录中，该子目录位于与 HTML 页面相同的目录中，你可以这样嵌入它：

```html
<img src="images/dinosaur.jpg" alt="恐龙" />
```

### 备选文本
我们接下来要看的属性是 `alt`。它的值应该是图片的文本描述，用于在图片无法显示或者因为网速慢而加载缓慢的情况下使用。

```html
<img
  src="images/dinosaur.jpg"
  alt="The head and torso of a dinosaur skeleton;
  it has a large head with long sharp teeth" />
```

### 宽度和高度
你可以用 [width](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/img#width) 和 [height](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/img#height) 属性来指定你的图片的宽度和高度。它们的值是不带单位的整数，以像素为单位表示图像的宽度和高度。

```html
<img
  src="images/dinosaur.jpg"
  alt="The head and torso of a dinosaur skeleton;
  it has a large head with long sharp teeth"
  width="400"
  height="341" />
```

如果你在 HTML 中使用 `width` 和 `height` 属性来指定图片的实际大小，那么在下载图片之前，浏览器就知道需要为其留出多少空间。

### 图像标题
类似于[超链接](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Structuring_content/Creating_links#%E4%BD%BF%E7%94%A8_title_%E5%B1%9E%E6%80%A7%E6%B7%BB%E5%8A%A0%E6%94%AF%E6%8C%81%E4%BF%A1%E6%81%AF)，你可以通过给图片增加 `title` 属性来提供更多的信息。

```html
<img
  src="images/dinosaur.jpg"
  alt="The head and torso of a dinosaur skeleton;
  it has a large head with long sharp teeth"
  width="400"
  height="341"
  title="A T-Rex on display in the Manchester University Museum" />
```

这会给我们一个鼠标悬停提示，和链接标题一样：

<img src="https://cdn.nlark.com/yuque/0/2026/png/66845298/1775043748808-02a4e005-a735-484a-9be2-b6fd672e5e79.png" width="400" title="" crop="0,0,1,1" id="u50b14fbe" class="ne-image">

### 通过为图片搭配说明文字的方式来解说图片
使用 HTML 的 [<figure>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/figure) 和 [<figcaption>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/figcaption) 元素，为图片提供一个语义容器，在说明文字和图片之间建立清晰的关联。

```html
<figure>
  <img
    src="images/dinosaur.jpg"
    alt="The head and torso of a dinosaur skeleton;
    it has a large head with long sharp teeth"
    width="400"
    height="341" />

  <figcaption>
    A T-Rex on display in the Manchester University Museum.
  </figcaption>
</figure>
```

[<figcaption>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/figcaption) 元素告诉浏览器和辅助技术工具，这段说明文字描述了 [<figure>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/figure) 元素的内容。

### CSS 背景图片
你也可以使用 CSS 把图片嵌入网站中（JavaScript 也行，不过那是另外一回事了）。CSS 属性 [background-image](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Properties/background-image) 和其他的 `background-*` 属性是用来控制背景图片的。比如，要想为页面中的每个段落设置一个背景图片，你可以这样做：

```css
p {
  background-image: url("images/dinosaur.jpg");
}
```

按理说，这种做法相对于 HTML 中插入图片的做法，可以更好地控制图片和设置图片的位置，那么为什么我们还要使用 HTML 图片呢？如上所述，CSS 背景图片只是为了装饰——如果你只是想要在你的页面上添加一些漂亮的东西，来提升视觉效果，那 CSS 的做法是可以的。但是这样插入的图片完全没有语义上的意义，它们不能有任何备选文本，也不能被屏幕阅读器识别，等等。这就是 HTML 图片有用的地方了。

总而言之，如果图像对你的内容有意义，则应使用 HTML 图像。如果图像纯粹是装饰，则应使用 CSS 背景图片。

### 网页上的其他图形
我们已经了解到可以使用 [<img>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/img) 元素显示静态图像，或者通过使用 [background-image](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Properties/background-image) 属性来设置 HTML 元素的背景。你还可以动态生成图形，或在生成后对图像进行操作。浏览器提供了使用代码创建 2D 和 3D 图形的方法，以及包含来自上传文件或用户摄像头实时流的视频。以下是有关这些更高级图像主题的文章链接：

[Canvas](https://developer.mozilla.org/zh-CN/docs/Web/API/Canvas_API)：[<canvas>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/canvas) 元素提供了使用 JavaScript 绘制 2D 图形的 API。

[SVG](https://developer.mozilla.org/zh-CN/docs/Web/SVG)：你可以借助可缩放矢量图形（SVG）来使用线条、曲线和其他几何形状来渲染 2D 图形。借助矢量图形，你可以创建能够以任意尺寸清晰缩放的图像。

[WebGL](https://developer.mozilla.org/zh-CN/docs/Web/API/WebGL_API)：WebGL API 指南将帮助你入门 WebGL，这是用于 Web 的 3D 图形 API，可让你在 Web 内容中使用标准的 OpenGL ES。

[使用 HTML 音频和视频](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Structuring_content/HTML_video_and_audio)：与 `<img>` 类似，你可以使用 HTML 将 [<video>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/video) 和 [<audio>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/audio) 嵌入到网页中，并控制其播放。

[WebRTC](https://developer.mozilla.org/zh-CN/docs/Web/API/WebRTC_API)：WebRTC 中的 RTC 代表实时通信（Real-Time Communications），这是一种可以在浏览器客户端（对等方）之间进行音频/视频流和数据共享的技术。

## 视频和音频内容
### <video> 元素
你可以借助 [<video>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/video) 元素来轻松地嵌入视频。一个简单的例子如下：

```html
<video src="rabbit320.webm" controls>
  <p>
    你的浏览器不支持 HTML 视频。可点击<a href="rabbit320.mp4">此链接</a>观看。
  </p>
</video>
```

值得注意的特性有：

[src](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/video#src)：同 [<img>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/img) 元素的使用方式相同，`src`（来源）属性指向你想要嵌入到网页中的视频资源，它们的运作方式完全相同。

[controls](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/video#controls)：用户应当能够控制视频和音频的播放（这对于患有[癫痫](https://zh.wikipedia.org/wiki/%E7%99%AB%E7%97%AB#%E7%97%85%E5%9B%A0)的人来说尤为重要）。你必须使用 `controls` 属性来让视频或音频包含浏览器自带的控制界面，或者使用适当的 [JavaScript API](https://developer.mozilla.org/zh-CN/docs/Web/API/HTMLMediaElement) 构建自己的界面。至少，界面必须包括启动和停止媒体以及调整音量的方法。

[<video>元素内的段落](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Structuring_content/HTML_video_and_audio#video)：这个叫做后备内容，当浏览器不支持 `<video>` 元素的时候，就会显示这段内容，借此我们能够对旧的浏览器提供回退。你可以添加任何后备内容，在这个例子中我们提供了一个指向这个视频文件的链接，从而使用户至少可以访问到这个文件，而不会局限于浏览器的支持。

已嵌入视频文件的网页样式如下：

<img src="https://cdn.nlark.com/yuque/0/2026/png/66845298/1775044439954-b56faf3c-53f6-49f0-abdc-6b3090c13b47.png" width="589" title="" crop="0,0,1,1" id="uac1f3629" class="ne-image">

### <audio> 元素
[<audio>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/audio) 元素与 [<video>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/video) 元素的使用方式几乎完全相同，只有一些细微的差别，比如下面的边框不同，一个典型的例子如下：

```html
<audio controls>
  <source src="viper.mp3" type="audio/mp3" />
  <source src="viper.ogg" type="audio/ogg" />
  <p>你的浏览器不支持该音频，可点击<a href="viper.mp3">此链接</a>收听。</p>
</audio>
```

## HTML 表格
### 什么是表格？
表格是由行和列（表格数据）组成的结构化数据集，它让你快速简单地查找某个表示不同类型数据之间的某种关系的值。比如说，某个人和他的年龄，一天或是一周，当地游泳池的时间表。

<img src="https://cdn.nlark.com/yuque/0/2026/png/66845298/1775092931200-0d680b01-8738-47a8-9f6c-7d8521bf3546.png" width="491" title="" crop="0,0,1,1" id="u40d0249e" class="ne-image">

### 创建表格
1. 每一个表格的内容都包含在这两个标签中：[<table></table>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/table)。在你的 HTML 的 [<body>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/body) 中添加这些内容。
2. 在表格中，最小的内容容器是单元格，是通过 [<td>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/td) 元素创建的（其中“td”代表“table data”）。把下面的内容添加到你的表格标签中：

```html
<td>我是第一个单元格</td>
```

3. 如果想让这一行停止增加，并让单元格从第二行开始，我们需要使用 [<tr>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/tr) 元素（其中“tr”代表“table row”）。

```html
<tr>
  <td>我是第一个单元格</td>
  <td>我是第二个单元格</td>
  <td>我是第三个单元格</td>
  <td>我是第四个单元格</td>
</tr>
```

4. 为了将表格的标题在视觉上和语义上都能被识别为标题，你可以使用 [<th>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/th) 元素（其中“th”代表“table header”），用法和 `<td>`是一样的，除了它表示为标题，不是普通的单元格以外。进入你的 HTML 文件，将表格中应该是标题的 `<td>` 元素标记的内容，都改为用 `<th>` 元素标记。
5. 允许单元格跨越多行和列。表格中的标题和单元格有 `colspan` 和 `rowspan` 属性，可以实现这些效果。这两个属性接受一个没有单位的数字值，数字决定了它们的宽度或高度是几个单元格。比如，`colspan="2"` 会使单元格横跨两列。

```html
<table>
      <tr>
        <th colspan="2">Animals</th>
      </tr>
      <tr>
        <th colspan="2">Hippopotamus</th>
      </tr>
      <tr>
        <th rowspan="2">Horse</th>
        <td>Mare</td>
      </tr>
      <tr>
        <td>Stallion</td>
      </tr>
      <tr>
        <th colspan="2">Crocodile</th>
      </tr>
      <tr>
        <th rowspan="2">Chicken</th>
        <td>Hen</td>
      </tr>
      <tr>
        <td>Rooster</td>
      </tr>
    </table>
```

### 为表格中的列提供共同的样式
使用 <col> 应用样式

可以在 `<col>` 元素上一次性指定信息。`<colgroup>` 容器就在开始标记 `<table>` 下面，`<col>` 元素在 `<colgroup>` 容器内指定。定义了两个“样式列”，其中一个为第二列每列指定样式信息。没有为第一列设计样式，但仍必须包含一个空白的 `<col>` 元素，否则样式将只应用于第一列。

```html
<table>
  <colgroup>
    <col />
    <col style="background-color: yellow" />
  </colgroup>
  <tr>
    <th>数据 1</th>
    <th>数据 2</th>
  </tr>
  <tr>
    <td>加尔各答</td>
    <td>橙汁</td>
  </tr>
  <tr>
    <td>机器人</td>
    <td>爵士乐</td>
  </tr>
</table>
```

如果想将样式信息应用于两列，只需包含一个带有 `span` 属性的 `<col>` 元素即可，就像这样：

```html
<colgroup>
  <col style="background-color: yellow" span="2" />
</colgroup>
```

就像 `colspan` 和 `rowspan` 一样，`span` 需要一个无单位的数字值，用来指定让这个样式应用到表格中多少列。

### 使用 <caption> 为你的表格增加一个标题
你可以通过 [<caption>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/caption) 元素为你的表格增加一个标题，再把 [<caption>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/caption) 元素放入 [<table>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/table) 元素中。你应该把它放在 `<table>` 开始标签的下面。

```html
<table>
  <caption>
    侏罗纪时期的恐龙
  </caption>

  …
</table>
```

### 添加 <thead>、<tbody> 和 <tfoot> 结构
由于你的表格在结构上有点复杂，如果把它们定义得更加结构化，那会帮助我们更能了解结构。一个明确的方法是使用 [<thead>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/thead)、[<tbody>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/tbody) 和 [<tfoot>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/tfoot)，这些元素允许你把表格中的部分标记为表头、表体和表尾三部分。

要使用它们，应按以下顺序排列：

+ `<thead>` 元素必须包住表格的表头部分。一般是第一行，往往都是每列的标题，但是不是每种情况都是这样的。如果你使用了 [<col>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/col)/[<colgroup>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/colgroup) 元素，那么 `<thead>` 元素就需要放在它们的下面。
+ `<tbody>` 元素需要包住表格内容的主要部分（不是表头和表尾）。
+ `<tfoot>` 元素需要包住表格的表尾部分。一般是最后一行，往往是对前面所有行的总结。

```html
<!DOCTYPE html>
<html lang="en-US">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>My spending record</title>
    <link href="minimal-table.css" rel="stylesheet" type="text/css">
    <style>
        tbody {
          font-size: 90%;
          font-style: italic;
        }

        tfoot {
          font-weight: bold;
        }
    </style>
  </head>
  <body>
    <h1>My spending record</h1>
      <table>
        <caption>How I chose to spend my money</caption>
        <thead>
          <tr>
            <th>Purchase</th>
            <th>Location</th>
            <th>Date</th>
            <th>Evaluation</th>
            <th>Cost (€)</th>
          </tr>
        </thead>
        <tfoot>
          <tr>
            <td colspan="4">SUM</td>
            <td>118</td>
          </tr>
        </tfoot>
        <tbody>
          <tr>
            <td>Haircut</td>
            <td>Hairdresser</td>
            <td>12/09</td>
            <td>Great idea</td>
            <td>30</td>
          </tr>
          <tr>
            <td>Lasagna</td>
            <td>Restaurant</td>
            <td>12/09</td>
            <td>Regrets</td>
            <td>18</td>
          </tr>
          <tr>
            <td>Shoes</td>
            <td>Shoeshop</td>
            <td>13/09</td>
            <td>Big regrets</td>
            <td>65</td>
          </tr>
          <tr>
            <td>Toothpaste</td>
            <td>Supermarket</td>
            <td>13/09</td>
            <td>Good</td>
            <td>5</td>
          </tr>
        </tbody>
    </table>
  </body>
</html>
```

### 嵌套表格
在一个表格中嵌套另外一个表格是可能的，只要你包含完整的结构，包括 `<table>` 元素。这样通常是不建议的，因为这种做法会使标记看上去很难理解，对使用屏幕阅读的用户来说，无障碍性也降低了。以及在很多情况下，也许你只需要插入额外的单元格、行和列到已有的表格中。然而有时候是必要的，比如你想要从其他资源中更简单地导入内容。

```html
<table id="table1">
  <tr>
    <th>标题 1</th>
    <th>标题 2</th>
    <th>标题 3</th>
  </tr>
  <tr>
    <td id="nested">
      <table id="table2">
        <tr>
          <td>单元格 1</td>
          <td>单元格 2</td>
          <td>单元格 3</td>
        </tr>
      </table>
    </td>
    <td>单元格 2</td>
    <td>单元格 3</td>
  </tr>
  <tr>
    <td>单元格 4</td>
    <td>单元格 5</td>
    <td>单元格 6</td>
  </tr>
</table>
```

输出看起来是这样的：

<img src="https://cdn.nlark.com/yuque/0/2026/png/66845298/1775099511623-14c170d5-3fe1-476f-b2fe-9d31541bc8cd.png" width="556.6666445467216" title="" crop="0,0,1,1" id="uc9728574" class="ne-image">

### scope 属性 ---- 所在行或列的表头
[scope](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/th#scope) 属性，可以添加在 `<th>` 元素中，以告诉屏幕阅读器该表头的类型——它是所在行的表头，还是所在列的表头。回想一下我们前面的消费记录例子，你可以像这样明确地把表头定义为所在列的头部：

```html
<thead>
  <tr>
    <th scope="col">购买</th>
    <th scope="col">位置</th>
    <th scope="col">时间</th>
    <th scope="col">评价</th>
    <th scope="col">成本 (€)</th>
  </tr>
</thead>
```

而每一行都可以有一个像这样定义的标题（如果我们把行的标题和列的标题都加上）：

```html
<tr>
  <th scope="row">理发</th>
  <td>理发店</td>
  <td>12/09</td>
  <td>好主意</td>
  <td>30</td>
</tr>
```

屏幕阅读器会识别这种结构化的标记，并一次读出整列或整行。

`scope` 还有两个可选的值：`colgroup` 和 `rowgroup`。这些用于位于多个列或行的顶部的标题。

```html
<thead>
  <tr>
    <th colspan="3" scope="colgroup">衣物</th>
  </tr>
  <tr>
    <th scope="col">长裤</th>
    <th scope="col">裙子</th>
    <th scope="col">连衣裙</th>
  </tr>
</thead>
```

这同样适用于多个分组行的标题。

```html
<tr>
  <th rowspan="2" scope="rowgroup">荷兰</th>
  <th scope="row">阿姆斯特丹</th>
  <td>89</td>
  <td>34</td>
  <td>69</td>
</tr>
<tr>
  <th scope="row">乌特勒支</th>
  <td>80</td>
  <td>12</td>
  <td>43</td>
</tr>
```

### id 和 headers 属性
如果要替代 `scope` 属性，可以使用 [id](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Global_attributes#id) 和 [headers](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/td#headers) 属性来创建标题与单元格之间的联系。

`headers` 属性包含一个空格分隔的无序字符串列表，每个字符串对应 `<th>` 元素的唯一 `id`，这些 `<th>` 元素为数据单元格（`<td>` 元素）或另一个标题单元格（`<th>` 元素）提供标题。

这样，HTML 表格就明确定义了表格中每个单元格的位置，这些单元格由其所属的每列和每行的标题定义，有点像电子表格。为使其运行良好，表格确实需要列标题和行标题。

回到“2016 年 8 月出售的物品”示例，可以这样使用 `id` 和 `headers` 属性：

1. 为每个 `<th>` 元素添加一个唯一的 `id`。
2. 为每个作为子标题（即在其上方有一个标题元素）的 `<th>` 元素添加一个 `headers` 属性。其值是位于顶部并定义子标题的标题 `id`，在我们的示例中，列标题为“衣物”，行标题为“比利时”。
3. 为每个 `<td>` 元素添加一个 `headers` 属性，并以空格分隔的列表形式添加相关联的 `<th>` 元素的 `id`。像在电子表格中一样进行操作：找到数据单元格，然后搜索行和列的相应标题。指定 `id` 的顺序并不重要，但应保持一致，使其井井有条。

```html
<thead>
  <tr>
    <th id="clothes" colspan="3">衣物</th>
  </tr>
  <tr>
    <th id="trousers" headers="clothes">长裤</th>
    <th id="skirts" headers="clothes">裙子</th>
    <th id="dresses" headers="clothes">连衣裙</th>
  </tr>
</thead>
<tbody>
  <tr>
    <th id="belgium" rowspan="3">比利时</th>
    <th id="antwerp" headers="belgium">安特卫普</th>
    <td headers="antwerp belgium clothes trousers">56</td>
    <td headers="antwerp belgium clothes skirts">22</td>
    <td headers="antwerp belgium clothes dresses">43</td>
  </tr>
</tbody>
```

## HTML 中的表单和按钮
### 用户交互
到目前为止了解到用户与网页交互的几种方式：

+ [链接](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Structuring_content/Creating_links)可用于导航到同一页面或不同页面的不同内容部分。
+ [<video>和<audio>](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Structuring_content/HTML_video_and_audio) 元素通常含有播放/暂停、快进、回退等功能，这允许用户根据需要来消费媒体内容。

然而，这些功能通常更偏向于单向交互，让用户被动地消费内容。虽然这没问题，但 Web 是一种双向体验。网站用户会根据自己的喜好调整内容和服务的使用方式。他们可能会叫车、申请回电、提交反馈、进行投诉、网购商品并送货到家。

要实现这种双向交互体验，你需要使用按钮和表单。

### 按钮
按钮通常是通过 HTML 的 [<button>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/button) 元素创建的（有时也使用 [<input>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/input) 元素并将其 `type` 属性设置为 `button` 或 `submit` 值）。这些按钮用途广泛——你可以将它们与任意功能关联，实现什么功能只取决于你的想象力和编码能力。

按钮在网页上有几种用途。首先，它们可用于触发某些功能，这在创建用户界面（UI）控件时非常有用。

```html
<button>点击这里</button>
```

出现在 `<button></button>` 标签的文字会显示在按钮内部，并且浏览器会为其应用一些基础样式，使它默认看起来和表现得像一个按钮。

为了让这个按钮变得实用起来，你需要将它放入表单中（我们稍后将会讲解），或者为它添加一些 JavaScript。

### 表单的结构
表单是通过 [<form>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/form)、[<label>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/label)、[<input>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/input) 和 [<select>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/select) 等元素创建的。与简单的按钮相比，表单元素可以创建更复杂的控件——例如包含多个选项的下拉菜单，允许用户在不同的用户界面主题之间进行选择。

一个基础的表单包含以下三个部分：

+ 一个 [<form>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/form) 元素，用于包裹表单的所有内容。所有包含在 `<form></form>` 标签内的表单控件都属于同一个表单，它们的数据会在表单提交时一起发送。
+ 一对或多对 [<label>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/label) 元素与表单控件元素（通常是 [<input>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/input) 元素，但也有其他类型，例如 [<select>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/select)）：
    - 表单控件元素允许用户选择或者输入一些数据，这些数据将在表单提交时发送到服务器。
    - `<label>` 元素为表单控件提供一个标识标签，用于描述应在控件中输入的数据内容。
+ 一个 [<button>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/button) 元素，用于提交表单。

```html
<!doctype html>
<html lang="zh-CN">
  <head>
    <meta charset="utf-8" />
    <title>第一个表单</title>
  </head>
  <body>
    <form action="./submit_page" method="get">
      <h2>订阅我们的新闻简报</h2>
      <p>
        <label for="name">姓名（必填）：</label>
        <input type="text" name="name" id="name" required />
      </p>
      <p>
        <label for="email">邮箱（必填）：</label>
        <input type="email" name="email" id="email" required />
      </p>
      <p>
        <button>订阅新闻简报！</button>
      </p>
    </form>
  </body>
</html>
```

### <form>元素
[<form>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/form) 元素作为表单的外层容器，用于将所有的表单控件组织到一起。当点击 `<button>` 按钮时，所有在表单控件中填写的数据将会被提交到服务器。`<form>` 元素可以包含多个属性，我们在示例中使用的两个最重要的属性是：

+ `action`：包含一个路径，用于指定提交的表单数据将发送到哪个页面进行处理。稍后，当你提交表单时，你会在 URL 中看到 `/submit_page`。你还会收到一个 [404](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Reference/Status/404) 错误响应，因为处理数据的页面实际上并不存在，但目前这样做是没有问题的。
+ `method`：指定将表单数据发送到服务器时使用的数据传输[方法](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Reference/Methods)。现在你不必太过担心这个属性；当值为 `get` 时，数据会作为参数附加在 URL 的末尾进行发送。

检查提交的数据

1. 在单独的浏览器标签页打开示例，尝试输入姓名“Bob”，电子邮件地址为“bob@bob.com”。
2. 点击 `<button>`。

`action` 和 `method` 属性会使表单数据以下列 URL 形式提交：

```plain
/some/url/submit_page?name=Bob&email=bob%40bob.com
```

结构化表单

你可以在 `<form>` 元素中包含任意的 HTML 元素，用于组织表单控件本身，并为 CSS 样式提供可定位的容器，以便进行样式设置等操作。

在示例中，我们使用了一个[标题元素](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/Heading_Elements)（`<h2>`）来描述该表单的用途。

我们还将每一对输入框/标签和提交按钮分别放在一个单独的 [<p>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/p) 元素中，这样每一组控件就会独占一行上。这些元素默认是行内（inline）的，这意味着如果我们不这么做，所有的控件将会处于同一行上。

这是表单结构化的常见形式。一些人使用 `<p>` 元素来分割表单控件，一些人使用 [<div>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/div)、[<section>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/section) 甚至是 [<li>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/li) 元素。只要使用的元素在语义上合理，这些其实并没有太大区别。例如，将表单项分组放在不同的段落或者内容区块中，或者作为列表项是合乎语义的。但使用[块级引用元素](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/blockquote)、[侧边栏元素](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/aside)或者是[联系人地址元素](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/address)来表示就不太合适。

还有一个专门用来对表单控件进行分组的元素：[<fieldset>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/fieldset)。当表单较复杂，或需要把多个复选框、单选按钮归为一组时，它就非常有用。稍后我们会给出几个 `<fieldset>` 的示例。

### <input>元素
[<input>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/input) 元素表示用户在表单中输入的各种数据项

```html
<input type="text" name="name" id="name" required />
```

这些属性的含义如下：

+ `type`：指定要创建的表单控件类型。表单控件类型有很多，从各种简单的文本字段，到单选按钮、复选框等。当值为 `text` 时，会渲染一个可接受任意文本的基本文本框
+ `name`：为该数据项指定一个名称。当表单提交时，数据会以名值对（name/value pairs）的形式发送。一般来说，`name` 属性的值就是这个数据项的“名称”，而用户在文本框输入的数据就是这个数据项的“值”
+ `id`：指定一个用于标识该元素的 ID。在这里，它用于将该表单控件与对应的 `<label>` 标签关联起来
+ `required`：指定该表单控件在提交表单前必须填写。这应仅用于必填字段，而不应设置在可选字段上

你需要知道的是，有些输入类型的值并不是用户直接在字段中输入的。例如 [<input type="color">](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/input/color) 会显示一个取色器，你可以从中选择颜色；[<input type="radio">](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/input/radio) 会显示一个单选按钮，可以被选中也可以不被选中

对于单选按钮，一般需要在 `value` 属性中指定一个具体的值，表示当该按钮被选中时，提交到服务器的实际内容。注意，你可以在 `text` 和 `color` 等输入类型上也设置 `value` 属性，其效果是：表单控件在初次渲染完成时就预先填充这个值

特定类型的文本输入框

有许多专门用于处理特定类型数据的文本字段输入类型，例如：[<input type="number">](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/input/number)、[<input type="password">](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/input/password) 和 [<input type="tel">](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/input/tel) 等等

### <label>元素
如上所述，[<label>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/label) 元素为表单控件提供了标识性标签，用于描述应该在控件中输入的数据。你可以在 `<label>` 元素中放置任意文本内容，但这些内容应准确描述关联表单控件所期望的数据类型。标签与控件之间的关联方式是：给表单控件设置一个 `id` 属性，然后给 `<label>` 设置 `for` 属性，其值与该控件的 `id` 相同

例如，将一个 `<label>` 和一个 <input> 元素相关联：

```html
<label for="name">姓名（必填）：</label>
<input type="text" name="name" id="name" required />
```

`<label>` 元素的重要性体现在多个方面，尤其包括以下几点：

+ 当视力障碍用户使用屏幕阅读器浏览和操作网页内容时，屏幕阅读器在遇到每个控件时，会朗读与之关联的标签文本。这能让用户更容易理解每个控件需要输入什么内容
+ 它们允许用户不仅可以点击控件本身，还可以点击标签文本来聚焦表单控件。这对移动设备用户尤其有用，因为在触摸屏上用手指精确选择表单控件可能比较困难。在这种情况下，扩大 可点击区域 会非常有帮助

显式与隐式表单标签

你在上文中看到的标签样式被称为显式表单标签——控件与标签之间的关联是通过 `id` 和 `for` 属性显式建立的。你也可以通过将控件嵌套在标签内的方式实现 隐式表单标签，如下所示：

```html
<label>
  姓名（必填）：
  <input type="text" name="name" required />
</label>
```

通过嵌套方式，控件与标签之间的关联是隐式建立的，因此你不再需要使用 `id` 和 `for` 属性。

这两种方式都可以使用，但我们建议你使用显式标签的方式。因为显式标签关联更容易识别和理解，尤其当你的 HTML 代码变得复杂时。此外，屏幕阅读器（以及其他辅助技术）有时不能正常处理隐式标签。

### <button>元素
当一个 [<button>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/button) 元素被放在 `form` 元素中时，它的默认行为是提交表单，只要没有无效数据阻止客户端表单验证。你在之前的基础表单示例中已经见过了这种行为。

通过 `<button>` 元素的 `type` 属性可以指定按钮的其他行为：

+ `<button type="submit">` 明确声明该按钮是“提交按钮”。一般来说不需要显式声明，除非你的 `<form>` 中包含了多个按钮，并且你想明确表示哪个按钮是用于提交表单的。这种情况非常罕见。
+ `<button type="reset">` 创建一个重置按钮——这会立即清空表单中输入的所有内容，将表单恢复到初始状态。不建议使用重置按钮——在早期的网页中它们比较常见，但通常会造成更多困扰。许多人曾经经历过填写完长长的表单后，不小心点击了“重置”按钮而不是“提交”，结果只能重新填写表单。
+ `<button type="button">` 创建一个普通按钮，其行为和 `<form>` 外的按钮一样。正如之前所见，普通按钮默认什么都不做，需要使用 JavaScript 来给它们添加功能。

> 备注：你也可以通过 `<input>` 元素配合不同的 `type` 属性来创建上述三种按钮：[<input type="submit">](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/input/submit)、[<input type="reset">](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/input/reset) 和 [<input type="button">](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/input/button)。但与 `<button>` 相比，它们存在许多限制，因此推荐使用 `<button>` 元素。
>

### 其他控件类型
有很多其他类型的控件可以用来在表单中收集数据。我们来看一个稍微复杂点的例子，然后对其逐步解析和说明。

备注：在这个例子中，我们假设用户已经注册并处于登录状态，因此无需收集姓名和邮箱地址等信息。

```html
<!doctype html>
<html lang="zh-CN">
  <head>
    <meta charset="utf-8" />
    <title>第二个表单</title>
  </head>
  <body>
    <form action="./payment_page" method="get">
      <h2>报名参见见面会</h2>
      <fieldset>
        <legend>选择酒店房型：</legend>
        <div>
          <input
            type="radio"
            id="hotelChoice1"
            name="hotel"
            value="economy"
            checked />
          <label for="hotelChoice1">经济型（+$0）</label>

          <input type="radio" id="hotelChoice2" name="hotel" value="superior" />
          <label for="hotelChoice2">高级型（+$50）</label>

          <input
            type="radio"
            id="hotelChoice3"
            name="hotel"
            value="penthouse"
            disabled />
          <label for="hotelChoice3">顶级套房（+$150）</label>
        </div>
      </fieldset>
      <fieldset>
        <legend>要参加的课程：</legend>
        <div>
          <input type="checkbox" id="yoga" name="yoga" />
          <label for="yoga">瑜伽（+$10）</label>

          <input type="checkbox" id="coffee" name="coffee" />
          <label for="coffee">咖啡烘焙（+$20）</label>

          <input type="checkbox" id="balloon" name="balloon" />
          <label for="balloon">气球动物艺术（+$5）</label>
        </div>
      </fieldset>
      <p>
        <label for="transport">出行方式：</label>
        <select name="transport" id="transport">
          <option value="">--请选择一项--</option>
          <option value="plane">乘坐飞机</option>
          <option value="bike">骑自行车</option>
          <option value="walk">徒步</option>
          <option value="bus">乘坐公交</option>
          <option value="train">搭乘火车</option>
          <option value="jetPack">使用喷气背包</option>
        </select>
      </p>
      <p>
        <label for="comments">其他备注：</label>
        <textarea id="comments" name="comments" rows="5" cols="33"></textarea>
      </p>
      <p>
        <button>去结账</button>
      </p>
    </form>
  </body>
</html>
```

呈现的效果如下：

单选按钮

“选择酒店房型”按钮是通过 [<input type="radio">](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/input/radio) 控件实现的。这些控件会渲染为一组按钮控件，每次只能选择其中一个——你不能同时选中多个。它们的名字来源于老式收音机上的按钮：按下一个按钮，之前选中的按钮就会弹出。

```html
<fieldset>
  <legend>选择酒店房型：</legend>
  <div>
    <input
      type="radio"
      id="hotelChoice1"
      name="hotel"
      value="economy"
      checked />
    <label for="hotelChoice1">经济型（+$0）</label>

    <input type="radio" id="hotelChoice2" name="hotel" value="superior" />
    <label for="hotelChoice2">高级型（+$50）</label>

    <input
      type="radio"
      id="hotelChoice3"
      name="hotel"
      value="penthouse"
      disabled />
    <label for="hotelChoice3">顶级套房（+$150）</label>
  </div>
</fieldset>
```

`radio` 输入控件的工作方式大致和 `text` 输入控件相同，但也有几点不同：

+ 每组单选按钮的 `name` 属性值必须相同，以便将它们关联成一组。如果 `name` 属性值不同，它们会被视为不同的组，提交时也会有发送不同的值。
+ 每个单选按钮必须包含一个 `value` 属性，用于指定提交时该按钮对应的值。提交的数据会是一个名值对，其中名称（即 `name`）始终相同，例如 `hotel=economy` 或 `hotel=superior`。
+ 每个单选按钮的 `<label>` 应该描述该具体选项的值，而不是你正在选择的这一组选项所代表的字段含义。描述整组选项的推荐做法是使用 [<fieldset>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/fieldset) 元素包裹这些选项，并用其子元素 [<legend>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/legend) 来提供整体描述。

> 备注：除了用于结构化和标记表单外，fieldset 还有其他用途，例如可用于一次性[禁用](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Structuring_content/HTML_forms#%E7%A6%81%E7%94%A8%E8%A1%A8%E5%8D%95%E6%8E%A7%E4%BB%B6)整组控件。
>

还值得注意的是，我们为第一个单选按钮添加了 `checked` 属性——这会让它在页面初次加载时默认被选中。这意味着总会有一个选项被选中，并且你无法取消选中一个单选按钮，除非选择另一个。

禁用表单控件

在单选按钮的示例中，你会注意到第三个单选按钮设置了 `disabled` 属性。这会导致该控件显示为灰色且无法被选中。这在很多情况下都非常有用，比如某个选项通常是可用的，但目前暂时不可用。例如，某个产品可能已经售罄，或者像我们示例中那样，顶层套房全部预订完毕！

你可以在任何表单控件上设置 `disabled` 属性，包括 `<button>` 元素。`<fieldset>` 元素也可以接受 `disabled` 属性——这会导致该 `<fieldset>` 内的所有表单控件都被禁用。

复选框

“选择要参加的课程”的复选框是使用 [<input type="checkbox">](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/input/checkbox) 控件实现的。这些控件渲染为一组开关状态的复选框。与单选按钮不同，你可以同时选择多个选项。

```html
<fieldset>
  <legend>选择要参加的课程：</legend>
  <div>
    <input type="checkbox" id="yoga" name="yoga" />
    <label for="yoga">瑜伽（+$10）</label>

    <input type="checkbox" id="coffee" name="coffee" />
    <label for="coffee">咖啡烘焙（+$20）</label>

    <input type="checkbox" id="balloon" name="balloon" />
    <label for="balloon">气球动物艺术（+$5）</label>
  </div>
</fieldset>
```

正如你在代码片段中看到的，单选按钮和复选框的实现方式非常相似（它们都可以使用 `checked` 属性，在页面加载时默认被选中）。它们的行为也比较类似，不同点在于单选按钮允许你从多个选项中选择零个或一个，而复选框允许你从多个选项中选择零个或多个。

主要区别（除了 `type` 属性值的不同）在于每个复选框的 `name` 属性值不同，且通常没有设置 `value` 属性。这意味着，每个复选框代表不同的数据值，而单选按钮只能代表一个值。当表单提交时，如果复选框被选中，则提交的值为 `on`，例如：`yoga=on`、`ballon=on` 等等。

> 备注：你可以通过为复选框添加 `value` 属性来自定义提交的值，例如：`<input type="checkbox" id="yoga" name="yoga" value="yes" />` 被选中时，会提交 `yoga=yes`。不过，这样做意义不大。复选框要么提交一个固定值（如果选中），要么不提交。提交给服务器的具体值其实并不重要。
>

下拉菜单

下拉菜单，比如我们示例中的“出行方式”选择控件，不是通过 `<input>` 类型实现的，而是使用 [<select>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/select) 和 [<option>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/option) 元素来实现的：

```plain
<label for="transport">出行方式：</label>
<select name="transport" id="transport">
  <option value="">--请选择一项--</option>
  <option value="plane">乘坐飞机</option>
  <option value="bike">骑自行车</option>
  <option value="walk">徒步</option>
  <option value="bus">乘坐公交</option>
  <option value="train">搭乘火车</option>
  <option value="jetPack">使用喷气背包</option>
</select>
```

`<select>` 元素囊括了所有不同的选项值。你需要在这里设置 `id` 属性，将控件与其标签关联起来，同时设置 `name` 属性，指定提交时数据项的名称。

数据项的每个可能值由嵌套在 `<select>` 内的 `<option>` 元素表示。每个 `<option>` 元素可以带有 `value` 属性，指定如果该选项被选中时提交的值。如果未指定 `value`，则使用 `<option></option>` 标签内的文本内容作为提交值。

> 备注：如果你想在页面加载时默认选中某个选项，可以在对应的 `<option>` 元素上添加 `selected` 属性。
>

多行文本输入框

多行文本输入框使用 [<textarea>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements/textarea) 元素创建

```plain
<label for="comments">其他备注：</label>
<textarea id="comments" name="comments" rows="5" cols="33"></textarea>
```

它们的行为与 `<input type="text">` 元素类似，不同之处在于它们允许输入多行文本。

+ `rows` 属性指定文本区域默认显示的行数
+ `cols` 属性指定文本区域默认显示的列数
+ 如果未指定这两个属性，浏览器默认使用 `cols="20"` 和 `rows="2"`

### 表单验证
前面我们已经了解了浏览器会提供一些基本的客户端表单验证功能。`required` 属性用于指定某个字段必须填写，才能提交表单；它还会检查某些特定类型的字段（例如电子邮件地址、URL、数字等）是否输入了正确的值。表单验证之所以重要，主要有两个原因：

+ 确保提交的数据格式正确，从而避免在应用程序中引发错误。
+ 防止数据引发安全问题。恶意用户可能会提交特意构造的数据，在不安全的应用中，这些数据可能会执行删除数据库或控制系统等命令。

需要注意的是，表单验证主要有两种类型：

+ 客户端验证：在浏览器端进行，通常通过表单验证属性（如 `required`）和 JavaScript 结合实现。客户端验证可以即时提示用户输入有误，但它并不可靠，不能有效阻止恶意数据。因为用户可以关闭 JavaScript 或修改客户端代码，从而绕过验证。
+ 服务器端验证：在服务器上进行，使用服务器端所采用的任意语言实现。错误格式的数据可以是意外发送的，也可以是有意而为之。经验法则是：服务器永远不要信任客户端发送的任何数据，以避免由于格式错误的消息而引发漏洞或安全问题。服务器端验证更适合阻止恶意消息，因为服务器端代码更难被篡改。但它无法像客户端验证那样及时给用户反馈，因为数据必须先发送到服务器验证，服务器再把结果返回给用户。

简而言之，不要只选择客户端验证或服务器端验证——你需要两者结合。你需要客户端验证来为用户的输入提供即时反馈；同时也需要服务器端验证，来确保发送到服务器的消息格式是安全、可处理的。如果你想开始深入学习表单验证，可以从[客户端表单验证](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Extensions/Forms/Form_validation)开始。