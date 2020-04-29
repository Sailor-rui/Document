在本地创建仓库并且连接了github的远程库后，在提交代码之后会出现更新被拒绝的错误 
导致出现这个的原因是因为本地仓库没有更新远程仓库中的内容。
所以我们需要用git pull origin master指令将远程代码库与本地代码库同步一下，但是可能会出现“fatal：拒绝合并无关历史。”的错误 
此项错误是由于本地仓库和远程有不同的开始点，也就是两个仓库没有共同的 commit 出现的无法提交。这里我们需要用到 --allow-unrelated-histories。也就是我们的 pull 命令改为下面这样的：
git pull origin master --allow-unrelated-histories
如果设置了默认分支，可以这样写
git pull --allow-unrelated-histories
