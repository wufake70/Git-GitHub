# 创建GitHub远程仓库

## 使用https 推送到远程库
### 1.添加远程库地址
* ```
    # origin 为远程地址的别名
    git remote add origin https://github.com/wufake70/ComputerNetworkLevel3.git
* 查看远程库地址
* ```
    git remote -v

### 2.开始推送
* ```
    # 注意: 该推送会在远程仓库创建一个新的分支
    git push origin master
### 3.GitHub上查看
* 在对应的远程仓库中选择`对应的分支`即可查看
### 4.gitignore忽略一些文件
* 对于一些不需要Git管理的文件，可以将其路径填写到.gitignore文件上
* ```
    # 不需要管理 temp.log,就可以在.gitignore 内添加一行 
    temp.log
    # 可以使用 *符号通配
    # 若是一个目录temp，及其子目录、文件等都不需要管理
    temp/
* 使用 `git status --ignored`查看已被忽略的文件
* 注意：.gitignore生效的前提是这些文件和目录都没有被git追踪
* 可以使用 `git rm`移除一些已被追踪的文件
* ```
    -f 或 --force：强制删除已被修改或已添加到暂存区的文件。
    -n 或 --dry-run：演示运行，展示哪些文件将被删除，但不实际执行删除操作。
    -r：递归删除指定目录及其子目录中的文件。
    --cached：仅从暂存区中移除文件，但保留工作目录中的文件。
* 在移除已被追踪的文件后 使用 `git commit -m "本次提交的描述信息" `提交删除操作