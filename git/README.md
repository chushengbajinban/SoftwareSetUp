### 作用
分布式版本控制系统

### 参考链接

[创建版本库 - 廖雪峰的官方网站](https://www.liaoxuefeng.com/wiki/896043488029600/896827951938304)



### 安装

windows: [Git - Downloads](https://git-scm.com/downloads)


### SSH 公钥配置
#### Windows
1. 新建一个目录，利用git工具打开 Git Bash Here

2. 执行如下命令"email@email.com" 其中邮箱为GitHub的邮箱,连续点击回车键即可
```
ssh-keygen -t rsa -C
``` 

3. 在后台启动 ssh-agent  
```
eval $(ssh-agent -s)
```

4. 将SSH私钥添加到 ssh-agent
```
ssh-add /c/Users/chenjs/.ssh/id_rsa
```

5. 先复制SSH公钥的完整内容（/c/Users/10071/.ssh/id_rsa.pub）
```
clip < /c/Users/10071/.ssh/id_rsa.pub
```

6. 进入GitHub的设置页面（登录GitHub，在右上角）,点击左部侧边栏的 SSH keys 选项,点击 Add SSH key 按钮；在Title输入框内，为你的新key取个名字，在Key输入框内，粘贴前面复制好的公钥内容，然后点击 Add key 按钮即可

7. 配置git全局信息
```
git config --global user.name “chushengbajinban” 
git config --global user.email “1007199462@qq.com” 
```