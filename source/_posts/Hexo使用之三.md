# Hexo使用之三

## 迁移到新设备

### Hexo文件解构

### Git Hexo





## 添加评论系统

已有其他平台稳定外联

###  平台比较

#### 第三方pinglunxitong

#### 基于git issue

##### gitment

##### gitalk



### gitment

## 其他

######  hexo d -g

```powershell
fatal: unable to access 'https://github.com/tailor997/tailor997.github.io.git/': OpenSSL SSL_connect: Connection was reset in connection to github.com:443
FATAL Something's wrong. Maybe you can find the solution here: https://hexo.io/docs/troubleshooting.html
Error: Spawn failed
    at ChildProcess.<anonymous> (F:\Project\Hexo\node_modules\_hexo-util@1.9.0@hexo-util\lib\spawn.js:51:21)
    at ChildProcess.emit (events.js:310:20)
    at ChildProcess.cp.emit (F:\Project\Hexo\node_modules\_cross-spawn@7.0.2@cross-spawn\lib\enoent.js:34:29)
    at Process.ChildProcess._handle.onexit (internal/child_process.js:275:12)
```

解决操作

```shell
git config --global --unset http.proxy 
git config --global --unset https.proxy
```

