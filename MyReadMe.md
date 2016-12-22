理解使用：
在指定目录 git clone 
通过
```shell
ln -s ${SRC_HOME}/CodeSnippets ~/Library/Developer/Xcode/UserData/CodeSnippets
```
先备份Xcode自带的CodeSnippets目录，然后创建一个替身来指定版本库中的CodeSnippets目录


这样以后在Xcode 中任意新建的CodeSnippets都会自动保存在版本库中

总结：
只需要一次setup_snippets.sh，以后只需要`git push` ，`git pull`维护版本库的更新即可














