#回退暂存区文件
1. git reset HEAD -- .
2. git rm --cached filename
-----
#回退版本
1. git reset --hard 索引值
![avatar](~/Pictures/1.png)
2. git reset --hard HEAD^
![avatar](~/Pictures/2.png)
3. git reset --hard HEAD~1
![avatar](~/Pictures/3.png)
-----
#合并分支
##merge
1. git branch yakumo
2. git checkout yakumo
3. git commit -m"commit message"
4. git checkout master
5. git merge yakumo
##rebase
1. git branch kochiya
2. git checkout kochiya
3. git commit -m"commit message"
4. git rebase master