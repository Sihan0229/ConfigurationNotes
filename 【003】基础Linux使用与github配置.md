

# Linux环境配置

 [Linux 创建 Python 虚拟环境](https://www.cnblogs.com/AllenMi/p/16367557.html)

 [把正在运行的程序放到后台继续](https://blog.51cto.com/lhrbest/5095909)

# git使用

[生成新的 SSH 密钥并将其添加到 ssh-agent](https://docs.github.com/zh/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

```bash
git config --global user.name 'YourGithubName'
git config --global user.email "your_email@example.com"
ssh-keygen -t ed25519 -C "your_email@example.com"
```

+ 确认路径和密码，可以不设置密码直接回车。
+ 随后进入刚刚确认的路径
+ 打开新生成的pub文件
+ 复制里面所有内容
+ 在github里点击右上角头像
+ 选择Settings
+ 选择SSH and GPG keys
+ New SSH KEY新建密钥
+ 起一个名字并且把刚刚复制的内容粘贴到Key文本框即可。
