# scripts
nothing but my scripts for doing, 2019.9



## json, viewer

一个好用的 JSON Viewer：https://codebeautify.org/jsonviewer



## git

make some rules

```
release v1.0

add xxx
update xxx
del xxx
change xxx

init the xx time

add xxx;del xxx
```

if forget, just go and find it out: https://git-scm.com/

```
git --version

git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
git config --global core.editor "'C:/Program Files/Notepad++/notepad++.exe' -multiInst -
nosession"
git config --list

git checkout 2-3
git checkout 2-3 -f

git diff 1-1 2-3
git diff origin/1-1 origin/2-3

git help config
git add -h

git init
git clone
git status
git add xx.md
gir rm xx.md
git commit -m 'the first commit'
git commit -a -m 'the first commit'

git log
git log --pretty=oneline

git tag
git tag -a v1.0 -m"v1.0"
git push --tags

git remote -v
git remote add name url
git remote rename oldname newname
git remote remove name


git branch
git branch -a
git branch newbranch
git branch checkout --orphan newbranch
git branch -m oldbranch newbranch

git checkout master
git checkout -

git merge newbranch
git pull origin newbranch
# refusing to merge unrelated histories
git pull origin newbranch --allow-unrelated-histories
git push orgin newbranch

git branch -d newbranch
git branch -d -r newbranch
git push -d orgin newbranch


#   usage: git branch [<options>] [-r | -a] [--merged | --no-merged]
#   or: git branch [<options>] [-l] [-f] <branch-name> [<start-point>]
#   or: git branch [<options>] [-r] (-d | -D) <branch-name>...
#   or: git branch [<options>] (-m | -M) [<old-branch>] <new-branch>
#   or: git branch [<options>] (-c | -C) [<old-branch>] <new-branch>
#   or: git branch [<options>] [-r | -a] [--points-at]
#   or: git branch [<options>] [-r | -a] [--format]

#    -m, --move            move/rename a branch and its reflog
#    -M                    move/rename a branch, even if target exists
#    -c, --copy            copy a branch and its reflog
#    -C                    copy a branch, even if target exists
#    -a, --all             list both remote-tracking and local branches
#    -d, --delete          delete fully merged branch
#    -D                    delete branch (even if not merged)
#    -r, --remotes         act on remote-tracking branches

```



## ubuntu, gnu/Linux

启动VPN

```
sslocal -c /etc/shadowsocks/config.json
```

解决无法使用：html5无法播放等

```
sudo apt-get install ubuntu-restricted-extras
```

解决中断报错：unable to lock..., is another process using it?

```
sudo rm /var/cache/apt/archives/lock 
sudo rm /var/lib/dpkg/lock

可能还需要执行下面这行代码进行修复
sudo dpkg --configure -a
```



## r

```
getwd()   显示当前的工作目录
setwd("mydirectory")  修改当前的工作目录为mydirectory
ls()  列出当前工作空间中的对象
rm(objectlist)  移除（删除）一个或多个对象
help(options)  显示可用选项的说明
options()  显示或设置当前选项
history(#) 显示最近使用过的#个命令（默认值为25）
savehistory("myfile")  保存命令历史到文件myfile中（默认值为.Rhistory）
loadhistory("myfile")  载入一个命令历史文件（默认值为.Rhistory）
save.image("myfile")  保存工作空间到文件myfile中（默认值为.RData）
save(objectlist, file="myfile")  保存指定对象到一个文件中
load("myfile")  读取一个工作空间到当前会话中（默认值为.RData）
q()  退出R
version 看R版本
install.packages("installr") 安装包，如果已经有此包可跳过此步骤
library(installr) 加载包，升级
updateR()	
ctrl + L 清空console

# R还是最亲切的
```



## python

工作路径相关

```
import os

os.getcwd()
os.chdir('')
```

第一个文件：say.py

> import sys
> txt = sys.argv[1]
> print (f'Hello {txt}!')

第二个文件：say2.py

> import sys
>
> for line in sys.stdin.readlines()：
>
> ​    print(f'Hello {line.strip()}!')

第三个文件：names.txt

> World
> water
> maomaol
> kenbing
> longer
> chuang

准备就绪，操作以下命令：

```
print('Hello World!')

python say.py World

cat names.txt | python say2.py # windows 下测试请使用 powershell

echo -e 'World\nwater\nmaomaol\nkenbing\nlonger\nchuang'|python say2.py
# windows 要改一下语句，具体参考 powershell 的语法
echo "World`nwater`nmaomaol`nkenbing`nlonger`nchuang"|python say2.py

cat names.txt | python say2.py > result.txt
```



## jupyter, notebook

安装插件

```
conda install -c conda-forge jupyter_contrib_nbextensions
```

去掉代码块

```
import IPython.core.display as di

di.display_html('<script>jQuery(function(){if(jQuery("body.notebook_app").length==0){jQuery(".input_area").toggle();jQuery(".prompt").toggle();}});</script>', raw = True)
```

前端相关

```
<script src="http://cdn.static.runoob.com/libs/jquery/1.10.2/jquery.min.js"></script>

-- jupyter导出html,jquery国内镜像
<script src="http://cdn.static.runoob.com/libs/jquery/1.10.2/jquery.min.js "></script>

-- jupyter导出html,jquery国外镜像
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>
```

魔法：%lsmagic

显示函数帮助：shift+tab



## conda

https://conda.io/docs/user-guide/getting-started.html

```
conda --version
conda update conda
conda info --envs
conda create --name snakes 
conda create --name snakes python=3.5
conda create --name snakes2 --clone abc

# change quickly, so read the doc will be fine
```

## pycharm template

```
#!/usr/bin/env python
# _*_coding:utf-8_*_
 
"""
@Time :    ${DATE} ${TIME}
@Author:  ${USER}
@File: ${NAME}.py
@Software: ${PRODUCT_NAME}
"""
```



## ruby

```
ridk install
```



## windows store

微软应用商店打不开闪退

情况说明：

- 手动删除一些C盘的文件，可能影响了应用商店。尝试修复无果。

可能的办法：

> 安装Microsoft Store
>
> 打开`powershell`以管理员身份运行；
>
> 输入命令：
>
> ```bash
> Get-AppXPackage *WindowsStore* -AllUsers | Foreach {Add-AppxPackage -DisableDevelopmentMode -Register "$($_.InstallLocation)\AppXManifest.xml"}
> ```
>
> 这样安装的应用商店是英文的，需要更新一下，会自动根据你的系统设置匹配语言（中文版）。
>
> 引自：https://beltxman.com/1936.html

解决的办法：

1. 运行上述代码，无报错，也无效果。
2. 尝试运行上述代码的开头部分：`Get-AppXPackage`。有列表返回，观察看到“**WinStore**”。
3. 修改上述代码。具体作法是将`*WindowsStore*`改为`*WinStore*`，再运行。有效果，成功打开。

