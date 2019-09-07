---
title: 學習日誌Day1
category: GithubXJekyll
order: 1
---
2019/9/7

## **git安裝**  
在使用[Github](https://github.com)與[Jekyll](https://jekyllrb.com/)之前，必需先安裝[Git](https://git-scm.com/), 先到官方網站安裝, 安裝完後可先在git bash產生SSH金鑰, 日後可以使用, 安裝方式可參考[這裡](https://help.github.com/en/enterprise/2.15/user/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)。

## **git與github基本操作**  
基本上有兩種版本管理的方式，一種是本機端的git，另一種為雲端上的github, 在使用上又可分為兩種方式如下:

>**從本機端建立專案再上傳到github**

step1:先在本機端建立一個資料夾並將專案放入  
step2:初始化Git版本管理  
`$git init`  
`$git add .`  
`$git commit -m 'description'`  
step4:在github建立新repository，在連到github上  
`$git remote add origin https://github.com/qwer987456/repositoryname.git`  
step5:將資料push上去  
`$git push -u origin master`

>**從github傳到本機端**

step1:先在本機端建立一個資料夾  
step2:在cmd上打`$git clone "git's repositories clone"`  

## **github branch 觀念**  
一個專案版分除了主線(master)，也可產生分支測試其他版本(branch)，在branch上的改變不會影響master的版本。[教學](https://www.youtube.com/watch?v=68CMwz3wMRE)  
`$git log --oneline --graph` 專案的架構  
`$git branch "branch.name"` 產生新的分支  
`$git branch` (check branch create)  
`$git checkout "branch.name"` (switch branch)  
`$git branch -d dev` (delete branch ps. Have to switch master status)  
`$git merge --no-ff -m "keep merge ing" "branch.name"` 將分支與主線結合 (--no-ff 留下訊息用的參數)  
`$git push --set-upstream origin dev` 將branch上傳到github上(或$git push origin "branch.name")  

## **Jekyll安裝**  
在windows上需要下在ruby，教學[在這](https://wcc723.github.io/jekyll/2014/01/13/windows-jekyll-server/)  
step1:`$gem update --system`  
step2:`$gem install jekyll`  
step3:`$jekyll server`  
ps:如果發生問題版本衝突時，使用`$gem uninstall`將衝突版本刪除