Git

**在github主页点击自己头像找到 Your repositories ，点击 Overview ，点击自己需要的仓库，点击 clone ，复制 Clone with SSH**

**---->**

**然后，打开 git ，使用命令 git clone （刚才复制的链接），然后本地就多了一个文件夹**

**---->**

**然后，如果自己要写的文件，写完之后，要上传到github仓库**

**---->**

**使用命令 git status ，检查本地中增加了哪些文件**

**---->**

**使用命令 git add . 把本地新增的内容上传到github缓存区**

**---->**

**使用命令 git commit -m 'project initialized'**

**---->**

**最后，使用 git push ，就能把增加的内容，上传到github仓库了。**





第二：

```
git add .

git commit -m "注释（可以任意）"
```

 最后就推送上去，输入以下命令



```
 git push origin master
```

把本地库的内容推送到远程，使用



```
 git push -u origin master 
```

**七、错误处理**

##### 在执行命令 git push origin master 时，报错 !



```
 [rejected] master -> master (non-fast-forward) error: failed to push some refs to 'git@gitee.com:***‘
```

意思是远程仓库的README.md 与本地没有合并。（建仓库的时候勾选了创建 README.md）

解决：

可以使用以下命令进行合并:



```
git pull --rebase origin master
```