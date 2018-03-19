创建dev分支，然后切换到dev分支：

```
$ git checkout -b dev
Switched to a new branch 'dev'
```
`git checkout`命令加上`-b`参数表示创建并切换，相当于以下两条命令：

```
$ git branch dev
$ git checkout dev
Switch to branch 'dev'
```

然后，用`git branch`命令查看当前分支：

```
$ git branch
* dev
  master
```

`git branch`命令会列出所有分支，当前分支前面会标一个`*`号。

然后，我们就可以在`dev`分支上正常提交：

```
$ git add readme.txt
$ git commit -m "barnch test"
[dev fec145a] branch test
1 file changed, 1 insertion(+)
```

现在，`dev`分支的工作完成，我们就可以切换回`master`分支：

```
$ git checkout master
Switch to branch 'master'
```

现在，我们把`dev`分支的工作成果合并到`master`分支上：

```
$ git merge dev
Updating d17ef8..fec145a
Fast-forward
  readme.txt |    1 +
  1 file changed, 1 insertion(+)
```

合并完成后，就可以删除`dev`分支了：

```
$ git branch -d dev
Delete branch dev (was fec1445a).
```

## 小结

Git鼓励大量使用分支：

查看分支：`git branch`

创建分支：`git branch <name>`

切换分支：`git checkout <name>`

创建 + 切换分支：`git checkout -b <name>`

合并某分支到当前分支：`git merge <name>`

删除分支：`git branch -d <name>`

