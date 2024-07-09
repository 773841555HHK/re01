# 常用git命令

以在文件夹下建立一个txt文件为例：

```
git version//查看git版本号
git config --global user.name "HHK"
git config --global user.email "1234567@qq.com"//设置用户名和邮箱 可以知道修改人的信息

git init //在当前目录初始化 创建一个隐藏文件夹
//Initialized empty Git repository in D:/HHK/HHK0/test1/.git/  初始化成功

git add test1.txt//添加方式1
git add .//添加方式2

//添加完成后 git只是暂时保存 还不会保存提交记录

git commit;//把暂时保存的变更 提交固定成一个版本
//回车后 打开终端编辑器 1.打开a或者i进入编辑模式 输入更改的说明 esc退出编辑模式 再输入英文冒号 输入wq 表示保存并退出
// 1 file changed, 1 insertion(+)  添加成功

git log //检查提交日志

//修改txt文件后 再次添加
git add .
git commit -m "fix(test):change content"//快速commit 同样的方式操作四次

//下载git history插件后 右键可以看见不同的git 版本


//如果想要回退到之前的版本 git log查询 复制想要退回的版本的 commitid 如0ce3411fac9a708051e17051f28d05d2c79f797e
git reset --hard 0ce3411fac9a708051e17051f28d05d2c79f797e//退回这次版本的状态 把后面的修改也清空了

//如果想要在不同版本间切换 可以用branch 即把当前版本复制一份
//先对文件进行修改
git branch 0.2//以此类推0.3 0.4

git branch -a//查看所有分支
git checkout 0.3//查看0.3分支
git checkout master//查看主分支

git merge 0.3//
```

