

# 基于Hexo的个人博客

### 1 Hexo介绍

Hexo 是一个快速、简洁且高效的博客框架。Hexo 使用 [Markdown](http://daringfireball.net/projects/markdown/)（或其他渲染引擎）解析文章，在几秒内，即可利用靓丽的主题生成静态网页。

> 个人博客地址：http://liangh.top/

### 2 环境准备

#### 2.1 node.js安装

node官网（<https://nodejs.org/en/>）下载对应系统安装包，按提示安装。

校验是否安装成功

```JS
$ node -v
$ npm -v
```

#### 2.2 git安装

Windows：git下载安装地址（<https://git-scm.com/download/win>）

校验是否安装成功

```JS
$ git --version
```

#### 2.3 hexo安装

hexo官方文档（<https://hexo.io/zh-cn/>）

```JS
$ npm install hexo-cli -g
$ hexo init blog
$ cd blog
$ npm install
$ hexo server
```

### 3 部署到github

#### 3.1 需要有个github账号xxx

#### 3.2 创建一个xxx.github.io的public仓库

例如您的账户名是xiaohong,则需要创建一个xiaohong.github.io的public仓库.

#### 3.3 安装hexo-deployer-git

```
$ npm install hexo-deployer-git --save
```

#### 3.4 修改配置文件

打开blog目录下的`_config.yml`文件进行配置

```
deploy:  
type: git  
repo: <repository url> #https://bitbucket.org/JohnSmith/johnsmith.bitbucket.io
branch: [branch] #published  
message: [message]
```

| 参数      | 描述                                                         |
| :-------- | :----------------------------------------------------------- |
| `repo`    | 库（Repository）地址                                         |
| `branch`  | 分支名称。如果您使用的是 GitHub 或 GitCafe 的话，程序会尝试自动检测。 |
| `message` | 自定义提交信息 (默认为 `Site updated: {{ now('YYYY-MM-DD HH:mm:ss') }}`) |

#### 3.5 部署

```
$ hexo d
```

### 4 设置GitHub Pages

进入xiaohong.github.io的setting配置中

拉到下面的GitHub Pages部分，选择master branch（主分支），点击save

刷新页面之后再回到GitHub Pages部分，可以看到页面已经发布，点击链接进入
