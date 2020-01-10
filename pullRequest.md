Back to [home page](README.md)  
Edit please visit: [Pull Request](https://github.com/BBong119/bbong119.github.io/blob/master/pullRequest.md)  


# Brief answer about two questions
> 是否可以多个collaborator承担review和approve任务？  
  
是的，所有Collaborator都有review和approve的权限，但是只要有一个人进行了merge/commit或者close操作，那这个pull request就算被处理了。所以这边建议是统一让一个用户来做Merge和Commit操作。  


> Collaborator可以在commit之前pull request吗？  

可以的，只要Collaborator不直接在主分支上提交代码，在自己的分支上提交之后再发起到主分支的pull request。Pull Request本质上就是Branch到Branch的合并。这个实现方式有两种：

***前提：代码储存在代码仓库RepoA，用于生成网页的源码的分支是RepoA的master分支*** 
* User A在更改代码前，先从RepoA拷贝（一键fork）当前仓库到新的仓库RepoB，改完代码之后从RepoB-master分支向RepoA-master分支发起Pull Request请求。  
* User A在更改代码前，直接在RepoA上新建一个分支Branch1，改完代码之后从从RepoA-Branch1分支向RepoA-master分支发起Pull Request请求。  
  
**第二种操作的话久了就会导致RepoA越来越大，或者要定期删除Branch（包含待处理的Pull Request的Branch无法删除）。所以比较推荐第一个方法。**


# Additional information about pull request review  

* Pull request权限：
    - 仓库的所有collaborators以及Pull Request发起者都可以访问Pull Request（即可以作为Reviewer）。
    - 仓库的所有collaborators都可以处理Pull Request（包括merge/commit或者close），即使TA是当前Pull Request的发起者。
 
* Reviewer可以对Pull Request做些什么：
    - 对每一个文件甚至某一行更改给出意见：  
![image loading failed](/pullRequestSrcPic/pullRequestReview.PNG)  
    - 给出自己对当前Pull Request的Decision（包括Comment/Approve/Request address）：  
![image loading failed](/pullRequestSrcPic/finalDecision.PNG)  
    - 看到所有Reviewers对当前Pull Request的Comments，并可以提出异议/要求重新Review（这里也可以是发起者做了修改提出重新Review请求）：  
![image loading failed](/pullRequestSrcPic/reviewer.PNG)   

  
* Pull request什么时候被处理：
    - 只有进行了commit或者直接close操作这个Pull Request才会关闭。
![image loading failed](/pullRequestSrcPic/closePullRequest.PNG)   


* Further Information:
    - 一个Pull Request将会对比两个分支所有有差异的文件，collaborator在merge的时候可以对每一处更改单独选择采用或弃用。
    - collaborator即使做为Pull Request的发起者，依旧拥有直接Merge和Commit的权限。
