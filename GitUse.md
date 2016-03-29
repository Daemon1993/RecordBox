- clone Repositories

 git clone url  当前目录中
 
 git clone url newdir 新建newdir目录

- 在整个git的操作流程中 file status 有

 untracked(未跟踪) 也就是本地新文件  
 
 unmodified(未修改) 本地与服务器一致 
 
 modified (已修改) 本地与服务器不一致
 
 staged (暂存区域) 只有在这个区域 才能commit

- 查看当前文件的状态
![文件状态 来自 git.oschaina.net](http://upload-images.jianshu.io/upload_images/831873-0afad151acf869fe.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


  进入当前项目 根目录 
  git status 列举
  新建一个文件 修改一个原始文件 git status 列表如下
  GitUse Untracked 
  README.md modified 已修改
  
![文件状态列表](http://upload-images.jianshu.io/upload_images/831873-08ee15e8c362a397.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 添加未跟踪的文件到暂存区域

 上面显示 changes to be commited 下的所有文件可以push到服务器了
  git add GitUse  
  
![git add之后](http://upload-images.jianshu.io/upload_images/831873-2d42d69d124044c4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![add 之后就是将文件添加到暂存区域](http://upload-images.jianshu.io/upload_images/831873-e80be7848ba494aa.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 查看当前暂存区域中的数据和上一次提交的也就是最新的之间的差异 

![查看当前更新详细情况](http://upload-images.jianshu.io/upload_images/831873-5b19d0d7b5dd8374.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- git commit 提交更新本地 push前一步
 
  git commit 进入Vim or 默认编辑器的界面 vim 按i(insert)插入相关message 

  git commit -m "提交信息"

![git commit提交更新](http://upload-images.jianshu.io/upload_images/831873-f6901686c93a6734.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 跳过使用暂存区域
-
 修改之后 可以不适用add 添加到暂存区 减少麻烦 直接使用下面 

 git -commit -a -m "message"  直接全部commit
 
![修改readme.md之后](http://upload-images.jianshu.io/upload_images/831873-1ffa7374f6aca977.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 移除文件 

git rm name

![git rm name](http://upload-images.jianshu.io/upload_images/831873-8b3d7e00d346f77c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 改名

  git mv oldname newName
  
![git mv之后的status显示](http://upload-images.jianshu.io/upload_images/831873-380e901dfbc146ef.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 查看提交历史

 git log 
 
![查看提交历史](http://upload-images.jianshu.io/upload_images/831873-e2b12f254f3cac16.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 取消添加到暂存区域的 文件

 git reset HEAD name
 
 这时候 git rm name是不能删除的
 
 只有 git rm -f name才能从暂存区删除



- push 上传服务器 默认 master分支 

 git push origin master
 
![push 服务器](http://upload-images.jianshu.io/upload_images/831873-f3675736dc137a6c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

 
