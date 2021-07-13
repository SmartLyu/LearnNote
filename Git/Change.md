

Git修改文本内容
===
增删改都属于修改文本，赠包括新建文本、文本添加内容，删包括删除文本、删除文本内容，改包括修改文本位置、修改文本内容。

在此提醒一个注意事项，在修改了git分支的操作后必须要提交，只有当`status`没有数据的时候才算写完了。

## 增删改文本内容、新建文本
修改完文件，需要先暂存`add`本地，再提交`commit`到本地分支。

## 删除文本
删除本地文本后，我们会发现`status`得到的结构是 D ，那么我们就需要从git体系中删除

```
git rm 文件名
git rm -f 文件名   ## 将暂存区中的文件内容也会删除
```
要注意，本地文件修改存储位置，以及重命名都会当做是删除了一个文本，创建了一个新的文本，git中移动文件和修改文件名，需要用特殊的方法。

除了我们手动产出本地文件外，也可以通过`git rm 文件`的方法，这样本地文件，和git本地分支文件都会被删除

## 移动文本、修改文本名
这个是根据linux的操作特点，移动文本，可以指定移动后的文件名，这样也就可以实现修改文本名，不过需要进行提交操作

```
git mv 原文件地址/名字  新文件地址/名字
git commit -m '提交修改位置(名字)'
```
