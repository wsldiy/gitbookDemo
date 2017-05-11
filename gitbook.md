# Gitbook培训 {#gitbook培训}

## 第一章 gitbook培训 {#第一章-gitbook培训}

### 1.1 gitbook简介 {#11-gitbook简介}

GitBook 是一个基于 Node.js 的命令行工具，可使用 Github/Git 和 Markdown 来制作精美的电子书。

GitBook可以把你的书本生成为静态网站以及PDF、ePub\(苹果和google的设备支持这种格式\)、Mobi\(kindle支持的格式\)格式的电子书。

### 1.2 gitbook章节和子章节 {#12-gitbook章节和子章节}

GitBook使用文件`SUMMARY.md`来定义书本的章节和子章节的结构。文件`SUMMARY.md`被用来生成书本内容的预览表。

`SUMMARY.md`的格式是一个简单的链接列表，链接的名字是章节的名字，链接的指向是章节文件的路径。

子章节被简单的定义为一个内嵌于父章节的列表。

简单实例:

```
# 概要

* [卷 I](part1/README.md)
    * [写作很棒](part1/writing.md)
    * [GitBook很酷](part1/gitbook.md)
* [卷 II](part2/README.md)
    * [期待反馈](part2/feedback_please.md)
    * [更好的写作工具](part2/better_tools.md)

```

### 1.2 gitbook类似工具 {#12-gitbook类似工具}

* kanCloud——专注于文档在线创作、协作、分享和托管

* eanpub——Publish Early, Publish Often

* penflip——在线文本编辑工具

## 第二章 gitbook安装使用 {#第二章-gitbook安装使用}

### 2.1 gitbook-cli的安装 {#21-gitbook-cli的安装}

GitBook 是一个基于 Node.js 的命令行工具；安装gitbook-cli需要首先安装nodeJS,安装gitbook-cli:

```
npm install gitbook-cli -g   #安装gitbook-cli

gitbook --version            #检测是否安装成功

```

![](https://hxgqh.gitbooks.io/haomotraining/content/assets/gitbookversion.png)

### 2.2 gitbook的使用 {#22-gitbook的使用}

创建gitbook书籍必须有 readme.md 和 summary.md文件；可以手动创建这两个文件，也可以使用 gitbook -init 自动创建:

```
cd ~/DeskTop/demo/gitbookDemo
gitbook init

```

![](https://hxgqh.gitbooks.io/haomotraining/content/assets/gitbookinit.png)

README.md 文件内容作为创建的gitbook的简介；

SUMMARY.md 文件内容为创建的gitbook的目录信息；

![](https://hxgqh.gitbooks.io/haomotraining/content/assets/readme.png)![](https://hxgqh.gitbooks.io/haomotraining/content/assets/summary.png)

再次使用`gitbook init`初始化文件夹如图：![](https://hxgqh.gitbooks.io/haomotraining/content/assets/gitbookinitfile.png)

这样我们在自己的电脑的；

当你在自己的电脑上编辑好图书之后，你可以使用Gitbook的命令行进行本地预览：`gitbook serve .`;之后，浏览器打开`localhost:4000`;如下图：![](https://hxgqh.gitbooks.io/haomotraining/content/assets/gitbookserve.png)![](https://hxgqh.gitbooks.io/haomotraining/content/assets/gitbookhtml.png)

`git build .`默认生成了\_book文件夹存储生成的html文件,可以使用：

```
git build . build   #生成build文件存储html文件

```

### 2.3 在线协作文档 {#23-在线协作文档}

gitbook可以帮助我们团队在线编写gitbook，协作编辑文档。

**tips:**首先要有git账号:

[gitbook地址](https://www.gitbook.com/)

[git地址](https://github.com/)

接下来登录gitbook,使用git账号登录：

![](https://hxgqh.gitbooks.io/haomotraining/content/assets/gitbooklogin.png)

进入主页选择点击create book，进入创建书籍页面，选择创建github类型书籍：

![](https://hxgqh.gitbooks.io/haomotraining/content/assets/gitbookhub.png)

点击图中2所指按钮，进入github页面；在github上安装gitbook；并创建gitbook相关创库：

![](https://hxgqh.gitbooks.io/haomotraining/content/assets/githubookinstall.png)![](https://hxgqh.gitbooks.io/haomotraining/content/assets/githubbuild.png)

接下里回到gitbook网站，新建书籍，选择github出现填写title等，选择刚才创建的仓库；然后点击`Create book`按钮，生成新的书籍；

![](https://hxgqh.gitbooks.io/haomotraining/content/assets/createbook.png)![](https://hxgqh.gitbooks.io/haomotraining/content/assets/bookjiemian.png)

这样我们就可以通过在github上上传我们创建的book，然后显示在gitbook上；

按照github上指示将本地创建的book上传到对应的仓库；

![](https://hxgqh.gitbooks.io/haomotraining/content/assets/gitpushbook.png)

在gitbook上刷新书籍我们就能看到这本书书籍了；在setting里通过添加成员并设置权限就可以实现多成员共同维护这本书籍了~

![](https://hxgqh.gitbooks.io/haomotraining/content/assets/showbook.png)![](https://hxgqh.gitbooks.io/haomotraining/content/assets/addmember.png)

