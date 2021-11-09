# 若你已经修改了部分文件、并且将其中的一部分加入了暂存区，应该如何回退这些修改，恢复到修改前最后一次提交的状态，给出至少两种不同的方式

**1.对于另一部分已经修改，但还位加入暂存区的文件，可以使用”git checkout --文件名“的命令回退到修改之前的版本
    对于已经加入暂存区的文件，则可以通过命令“git reset 文件名”将之前的"git add 修改 文件名“的操作撤销，使上传到暂存区的修改文件回退最后一次提交的状态，但需要注意，此时工作区修改的文件还是修改后的版本，使用“git checkout --文件名”将其回退到上一次提交的状态
【graph】/missing-semester/2021-finalproject/lionLJX/1.png

  2.面对想退回在暂存区的修改，我们还可以使用命令“git rm --cached 以修改文件名“的方式将暂存区中这个文件退回到第一次提交的 状态
【graph】/missing-semester/2021-finalproject/lionLJX/2.png


## 若你已经提交一个新版本，需要回退到该版本，应该怎么操作？分别给出不修改历史或修改历史的至少两种不同的方法

**1.不修改历史的方法
   a,使用命令“git commit --amend",执行该命令将弹出文本让你修改最后一次的修改，你可以将其修改回原来的版本，或者进行改进，修改后，再次commit,便成功提交出你想要呈现的仓库,(需对vi的基础操作有一定了解gi)
 【graph】/missing-semester/2021-finalproject/lionLJX/3.png
   b,使用命令“git revert -n 版本号”，撤回到该版本号的提交，之后进行修改后便可再次提交
 【graph】/missing-semester/2021-finalproject/lionLJX/4.png
**2.修改历史的方法
   a,使用命令“git reset --hard 目标版本号”将版本回退版本号可以通过命令“git log"来获得。此时便回到上一个版本，此时如果不想再进行修改，便可以自己使用git push -f强制推上去
 【graph】/missing-semester/2021-finalproject/lionLJX/5.png

## 我们已经知道了合并分支可以使用merge,但这不是唯一的方法，给出至少两种不同的合并的方式

**1.使用命令“git cherry-pick 分支名字",可以将指定的提交，应用于其他分支（主分支）。
  【graph】/missing-semester/2021-finalproject/lionLJX/6.png
  2.使用命令“git rebase 分支名字”
  【graph】/missing-semester/2021-finalproject/lionLJX/7个.png
  