理解使用：
在指定目录 git clone 
通过
```sh
ln -s ${SRC_HOME}/CodeSnippets ~/Library/Developer/Xcode/UserData/CodeSnippets
```
先备份Xcode自带的CodeSnippets目录，然后创建一个替身来指定版本库中的CodeSnippets目录


这样以后在Xcode 中任意新建的CodeSnippets都会自动保存在版本库中

总结：
在不同机子上使用统一的CodeSnippets，只需要一次`git clone`,` setup_snippets.sh`，以后只需要`git push` ，`git pull`维护版本库的更新即可


### 安装dmg

1. 先找到dmg安装文件路径` MOUNTDIR`
2.  installer -pkg即可
```sh
MOUNTDIR=$(echo `hdiutil mount Packages.dmg | tail -1 \
| awk '{$1=$2=""; print $0}'` | xargs -0 echo) \
&& sudo installer -pkg "${MOUNTDIR}/"*.pkg -target /
rm -rf "Packages.dmg"
```
> 注:当dmg中的安装文件是.app,直接食用cp命令:
```sh
cp -rf  Docker.app Applications
```



