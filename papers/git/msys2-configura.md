# MSys2 Git 配置问题

* 进入某个 Git 项目的目录时，不会显示当前所在的分支
* Git 子命令不支持 Tab 补全
* Vim 缺少默认配置文件

将文件Copy到对应的目录

file|target pwd
----|----
[bash_profile.sh](bash_profile.sh)|etc/profile.d/
[git-prompt.sh](git-prompt.sh)|etc/profile.d/
[vimrc](vimrc)|etc/profile.d/

然后修改 etc/bash.bashrc，找到这一行并在行首添加 # 将其注释：
```bash
PS1='\[\e]0;\w\a\]\n\[\e[32m\]\u@\h \[\e[35m\]$MSYSTEM\[\e[0m\] \[\e[33m\]\w\[\e[0m\]\n\$ '
```