---
title: hexo 博客折腾记 # 标题
date: 2025/2/2 hh:mm:ss # 时间
categories: # 分类
	- 技术  # 只能由一个
tags: # 标签
	- 个人博客  # 能有多个
	- web  # 一个标签一行
---

## 为什么写博客
1、功能  
放点自己常用的网站  
相册  
工具网站  
随笔：自己的一些思考  
放一些自己的作品集  
作为一个导航网站

2、体验网络建站的玩法  
部署  
网站托管  
自动发布  
域名啥的

## 静态博客和动态博客
静态博客：hexo  
动态博客：

## 关于博客的一些技术栈
+ cdn加速  
[https://blog.cuijiacai.com/blog-building/](https://blog.cuijiacai.com/blog-building/)  —hexo + netfily + 域名 + cloudflare（cdn加速）
+ github pages 网站托管平台

是一个静态网页托管网站，必须先生成静态网站的文件 才能托管  
GitPage 是 GitHub Pages 的简称，是 GitHub 提供的一项静态网站托管服务。它允许用户将仓库中的 HTML、CSS、JavaScript 等文件直接部署为网站，通常用于展示项目文档、个人博客或项目主页。

+ 静态网站生成器

除了 Jekyll，还有其他静态网站生成器可以搭建博客：  
Hugo：用 Go 编写，速度快  
Hexo：用 Node.js 编写，适合前端开发者  
常用的静态网站生成器有：  
Jekyll（适合博客、文档  
Hugo（速度快，适合大型网站）  
Hexo（基于 Node.js，适合前端开发者）  
Gatsby（基于 React，适合现代化网站）  
VuePress（适合文档类网站）

+ git action 了解下

最终我的部署方案是源Markdown文件提交到 GitHub ，利用 Github Actions 功能编写一个自动部署脚本。当master分支有内容提交时，触发脚本



## hexo 博客的一些缺点
1、文章可以分目录存放，但文章分类需要在文章中使用下面这种方式设置，不能设置使用目录树的方式

```plain
---
title: 随笔一则 # 标题
date: 2019/3/26 hh:mm:ss # 时间
categories: # 分类
    - test1  # 只能由一个
tags: # 标签
    - testTag  # 能有多个
    - TagGame  # 一个标签一行
---

```



2、不能在线编辑，需要在电脑上编辑之后使用hexo生成静态网站之后才能显示在网页上



## hexo 博客的搭建步骤


### hexo博客搭建：

[<font style="color:#dca10d;">https://developer.aliyun.com/article/1218122</font>](https://developer.aliyun.com/article/1218122)<font style="color:#000000;">  — 使用Hexo从0到1搭建个人博客详细教程（超详细，超简单）</font>

[<font style="color:#dca10d;">https://www.yangbing.fun/2019/06/29/save-hexo-source-post-with-git-branch/</font>](https://www.yangbing.fun/2019/06/29/save-hexo-source-post-with-git-branch/)<font style="color:#000000;"> —使用git分支保存hexo博客源码到github</font>

[<font style="color:#dca10d;">https://juejin.cn/post/6844904020306296845</font>](https://juejin.cn/post/6844904020306296845)<font style="color:#000000;">  </font><font style="color:#000000;">一键备份</font>



### next 主题优化：

[<font style="color:#dca10d;">https://sspai.com/post/85116</font>](https://sspai.com/post/85116)

[<font style="color:#dca10d;">https://blog.mrzorg.top/Hexo/2020-02-12-hero-next-theme-settings/</font>](https://blog.mrzorg.top/Hexo/2020-02-12-hero-next-theme-settings/)<font style="color:#000000;">  </font><font style="color:#000000;">— 高阶设置</font>

[<font style="color:#dca10d;">https://blog.csdn.net/mqdxiaoxiao/article/details/93644533</font>](https://blog.csdn.net/mqdxiaoxiao/article/details/93644533)<font style="color:#000000;"> —分类</font><font style="color:#000000;">	</font>


### 代码提交和发布
使用1个库+两个分支来管理代码，source分支保存源码，使用master分支保存生成的静态网站。平时的修改都推到source分支，deploy的时候生成静态网站然后将生成的代码推动到master分支上去

### nefify自动化部署
当source分支有提交的时候，使用hexo g命令自动编译并发布
https://yleave.github.io/2020/09/12/%E5%8D%9A%E5%AE%A2%E6%90%AD%E5%BB%BA/%E4%BD%BF%E7%94%A8Netlify%E9%83%A8%E7%BD%B2%E5%8D%9A%E5%AE%A2/


## hexo优秀实例


这个博主的博客页面非常好看：  
[https://shoka.lostyu.me/about/#678288218101ac2f442684d0](https://shoka.lostyu.me/about/#678288218101ac2f442684d0)



这个博主的内容非常丰富：   
[https://rawchen.com/music](https://rawchen.com/music)  
[https://pan.rawchen.com/](https://pan.rawchen.com/)  - 他还有云盘



好看的hexo主题推荐  
[https://juejin.cn/post/7053744641383874574](https://juejin.cn/post/7053744641383874574)



