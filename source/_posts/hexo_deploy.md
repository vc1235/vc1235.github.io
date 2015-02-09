title: "部署Hexo中遇到的问题"
date: 2015-02-06 11:33:53
tags: Hexo 
---
### node.js安装后NPM命令显示“Error: ENOENT, stat 'C:\Users\Administrator\AppData\Roaming\npm' ”

其实就是在相应文件夹新建npm文件夹就可以解决了。

---

### 安装hexo后，生成的首页是代码

貌似hexo某个版本就没加
hexo-renderer-ejs
hexo-renderer-marked
hexo-renderer-stylus
这些插件了，你可以在dependencies里面加上这些然后再install
或者当前目录运行npm install XXX(插件名) --save就好了
或者在当前目录执行
npm install

-----------
### hexo的备份

####安装[hexo-git-backup](https://github.com/coneycode/hexo-git-backup)
    $ npm install hexo-git-backup 

在github上创建branch
#### 在_config.yml中配置

    backup:
        type: git
        theme: coney
        repository:
        github: git@github.com:xxx/xxx.git,branchName
        #gitcafe: git@github.com:xxx/xxx.git,branchName

#### 使用

    $hexo b