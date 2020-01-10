Back to [home page](README.md)  
Edit please visit: [Pull Request](https://github.com/BBong119/bbong119.github.io/blob/master/pullRequest.md)  


> 是否可以多个collaborator承担review和approve任务？  
  
是的，所有Collaborator都有review和approve的权限，但是只要有一个人进行了merge/commit或者close操作，那这个pull request就算被处理了。所以这边建议是统一让一个用户来做Merge和Commit操作。  


> Collaborator可以在commit之前pull request吗？  

可以的，只要Collaborator不直接在主分支上提交代码，在自己的分支上提交之后再发起到主分支的pull request。Pull Request本质上就是Branch到Branch的合并。这个实现方式有两种：
前提：代码储存在代码仓库RepoA，用于生成网页的源码的分支是RepoA的master分支。  
* User A在更改代码前，先从RepoA拷贝（一键fork）当前仓库到新的仓库RepoB，改完代码之后从RepoB-master分支向RepoA-master分支发起Pull Request请求。  
* User A在更改代码前，直接在Repo A上新建一个分支Branch1，改完代码之后从从RepoA-Branch1分支向RepoA-master分支发起Pull Request请求。  

一个Pull Request将对比两个分支上所有的文件，对所有的更改统一处理，在Merge的时候Owner或者Collaborator可以对每一个修改单独选择采纳或丢弃。  


