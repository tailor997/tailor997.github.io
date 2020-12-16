# 在 GitHub Pages 上部署 Hexo

## 参考

- 官方：[在 GitHub Pages 上部署 Hexo](https://hexo.io/zh-tw/docs/github-pages.html)

- [搭建个人博客-hexo+github详细完整步骤](https://www.jianshu.com/p/189fd945f38f)
- [零基础免费搭建个人博客-hexo+github](https://blog.csdn.net/jzooo/article/details/46781805)

## 环境安装

### Git

- [Git下载地址](https://gitforwindows.org/)

- 默认安装
- 尽量Git、Node.js先后安装

### Node.js

- [Node.js下载地址](https://nodejs.org/en/)

- 默认安装

###### bash: npm: command not found

- 先安装Git、Node.js,重启一遍

### 安装Hexo

npm速度慢，被“墙”

```shell
# 换国内镜像
$ npm install cnpm -g --registry=https://registry.npm.taobao.org
# 使用淘宝NPM安装Hexo
$ cnpm install -g hexo-cli
```

> 与原先的npm完全一样，只是命令改为cnpm,一样等待hexo安装完成
> 出现的WARN可以不用理会

继续输入

```shell
$ cnpm install hexo --save
# 安装完成后，在输入命令，验证是否安装正确
$ hexo -v
```

### 初始化Hexo

- 创建文件夹
  - /Hexo
- 在Hexo文件下，右键运行Git Bash输入命令：

```shell
$ hexo init
```

- 配置_config.yml



## 本地运行

- Git Bash

```shell
# 运行hexo,以后要在本地运行博客只要输入该命令即可
$ hexo s -g

# 停止运行
Ctrl+C
```

- 浏览器输入：localhost:4000

## 部署到Github

- Github上：new repository:
  - tailor997.github.io

- 配置_config.yml：

```shell
# Deployment
## Docs: https://hexo.io/docs/deployment.html
deploy:
  type: git
  repo: https://github.com/tailor997/tailor997.github.io.git
# 有空格↑
```

- Git Bash

```shell
# 安装hexo-deployer-git自动部署发布工具
$ cnpm install hexo-deployer-git  --save
# 发布到Github
$ hexo clean && hexo g && hexo d
```

- 测试访问，浏览器：https://tailor997.github.io/

## 更新Blog

- 写文章

  \Hexo\source\\_posts文件下，新建.md文件就可以写文章

- Git Bash

```shell
# 发布更新博客
$ hexo d -g
```



##Wordpress迁移HEXO 

- WordPress 
  - 仪表盘中导出数据(“Tools” → “Export” → “WordPress”)
- Git Bash

```shell
# 安装 hexo-migrator-wordpress 插件
$ cnpm install hexo-migrator-wordpress --save
# 插件安装完成后，执行下列命令来迁移所有文章。source 可以是 WordPress 导出的文件路径或网址。
# hexo migrate wordpress <source>
# 注意目录
$ hexo migrate wordpress wordpress.2020-04-18.xml
$ hexo server
```

