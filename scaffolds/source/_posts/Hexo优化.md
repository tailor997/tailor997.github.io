## 主题

[Hexo官网的主题页](https://hexo.io/themes/)

GitHub关键词“hexo theme”

### [Yilia-plus](https://github.com/JoeyBling/hexo-theme-yilia-plus)

- 安装

```shell
cd blog
git clone https://github.com/JoeyBling/hexo-theme-yilia-plus
cd themes/yilia-plus
git pull
```

- 本地查看

```
$ hexo g -d  & hexo s
```

- 上传

```
$ hexo d
```

###### warning1

```shell
# Github Download ZIP 解压后
$ git pull
fatal: not a git repository (or any of the parent directories): .git
```

- 缺少 .git
- 可使用GitHub Desktop  clone ,copy.

> 在git 克隆代码之后，还不能直接使用git，而需要初始化git，它会自动创建git仓库需要的目录。这些文件存在于项目下的.git文件夹下。

###### warning2

- 多次安装主题，没效果

- 使用hexo clean ,再安装

### 侧边栏社交小图标

打开主题配置文件（`_config.yml`），搜索`social_icons:`,在 [图标库](http://fontawesome.io/icons/) 找自己喜欢的小图标，并将名字复制在如下位置，保存即可

## RSS

## 域名访问



- Dynadot
  - 注册zzhe.me
    - .me是黑山国家域名，一朝赛博南斯拉夫瓷
  - DNS设置
    - 自定义DNS

> 一开始选择 隐性转发 ，虽然便捷，但界面在移动端不适配。

- Github
  - 找到托管博客的`xxx.github.io`项目
  - 进入到设置页面，并滑动到下方，找到**Github Pages**这一栏，在**Custom Domain**填上刚刚添加解析的域名并保存：

#### 参考

[三步搞定Github Pages自定义域名](https://www.jianshu.com/p/2647e079741f)

## 评论

## MD差异

- .md文件名也做一级标题，故可在文章内省略一级标题

##  Other

[浅谈我为什么从 HEXO 迁移到 HUGO](https://sspai.com/post/59904)

看了篇文章，Hexo瞬间不香了，先用着主流的吧，坑少，省精力

