
# 配置环境

I2M实验室主页由基于ruby的博客框架jekyll搭建而成，我们使用的主题是修改版的solid。所以我们在维护或者建立
该博客时需要配置好以下环境。

1. ruby(+Devkit)：当前服务器上安装的版本是`ruby 2.4.4p296 (2018-03-28 revision 63013) [x64-mingw32]`
2. jekyll：当前安装的版本是`jekyll 3.8.3`
3. Github(Desktop or Git shell)

# 维护

1. 本地查看：启动ruby命令行窗口，进入博客所在目录。然后输入`jekyll server`或者`jekyll s`，此时博客就会被实时渲染。
可以在浏览器内输入`127.0.0.1:4000`，就可以在本地查看修改后的效果；
2. 部署远程：启动github desktop，然后左上角`add local repository`添加本地博客所在目录。填入commit message之后，点击Commit to master；然后在点击push origin推送到远程；
3. 输入对应的网址进行查看`usrname.github.io`
4. 推荐使用`VS code` 对项目进行维护。


# 更加具体

首先需要了解网站页面如何修改，以下给出整个工程的目录结构。

## Structure of this project

    Project root
    |   .gitignore		 // 指定推送远程可忽略的内容，一般不需要修改
    |   index.html         // 网站的全局设置
    |   projects.html      // 工程样式，一般不需要修改
    |   publications.html  // 已发表文章样式，一般不需要修改
    |   README.md		  // 本文档
    |   xinjin.html		// xinjin's resume	
    |   _config.yml		// 站点配置文件
    ├── assets
    |   ├── fonts
    |   ├── img
    |   |   |   footer-wordmark.png  // 网站最下方的logo
    |   |   |   xinjin.jpg // 老师头像
    |   |   ├── members    // 头像们
    |   |   └── projects   // 项目
    |   └──js
    ├── members            // 每个成员的详细页
    ├── _data
    |        members.yml         // 添加已有成员
    |        past_members.yml
    |        projects.yml
    |        publications.yml    // 添加已发表论文
    |        recent_members.yml  // 添加已毕业成员
    ├── _includes
    |   |    footer.html
    |   |    head.html
    |   |    js.html
    |   |    members.html      // 成员列表
    |   |    nav.html          // 导航栏
    |   |    past_members.html
    |   |    recent_members.html
    |   |    wrap.html
    |   └──css
    ├──  _layouts // 页面样式，一般不需要修改
    └── _site

## Members

To add a new member, edit `./_data/members.yml`. Add a new entry at the end of the file in the form:

```
- name: Shiyu Chang
  image: shiyu.jpg
  text:
  social:
    - title: envelope #use for email address
      url: mailto:chang87@illinois.edu
    - title: link
      url: http://www.ifp.illinois.edu/~chang87/
```

Then move the picture into `./assets/img/members`.

When you are done, push the changes.

## Recent Members

To add a Recent member, edit `./_data/recent_members.yml`. Add a new entry at the end of the file in the form:

```
- name: Haixu Han (2018)
  image: haixuhan.jpg
  text: Wechat Researcher
  social:
    - title: envelope #use for email address
      url: mailto:haixu.han@qq.com
    - title: link
      url: https://www.linkedin.com/in/%E6%B5%B7%E6%97%AD-%E9%9F%A9-ab5531139/
```
Note that the `url` can be `relative path`, eg.  `url: /members/haixuhan/`. Then you should edit the contents of the file in the path `/members/haixuhan.html`.

When you are done, push the changes.


## Projects

To add a new project, edit `./_data/projects.yml`. Add a new entry at the end of the file in the form:

```
- name: Project Name
  image: project-figure-name.png
  text: 'Description.'
```

Then move the picture into `./assets/img/projects`.

When you are done, push the changes.

## Publications

To add a publication, edit `./data/publications.yml`. Find the appropriate section (e.g. Books, Book Chapters, Journal Papers, etc), and add a new entry under articles. For example:

```
  - title: "Paper Title."
    authors: 'A. Author, T. Huang.'
    venue: 'Conference name'
    year: '2016'
```




