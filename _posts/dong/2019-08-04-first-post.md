---
layout: article
title: "Git"
date: 2019-08-04 13:30:00 -0400
categories: "dev-dong"
---
----------------------------------------
# Git Command \#1
   1. 브랜치 생성
<PRE><CODE>
git branch testB
git checkout testB
</CODE></PRE>
   2. Merge(현재 브랜치에서 testB 를 merge 함)
<PRE><CODE>
git merge testB
</CODE></PRE>
  3. Rebase(testB 브랜치에서 master브랜치로 rebase)
<PRE><CODE>
git checkout testB
git rebase master
git checkout master
git rebase testBranch
# master 브랜치는 Fast forward 됨 
</CODE></PRE>
# Rebase와 Merge의 차이
  - Rebase : 리베이스 하는쪽으로 모든 변경사항을 이동
    --결과 하나의 브랜치만 남음
  
  - Merge : 두 branch의 변경사항을 하나로 합침 
    --브랜치 히스토리에 두개의 브랜치가 하나로 합쳐졌음이 남음
  
# Case 별 가이드(해당 Local repo에서 win : git bash나 macOs : terminal 사용)
#### Case0. 최초 Branch Commit
      git init
      git add
      git commit -m 'initial commit'
      git push origin master
      
#### Case1. Single Branch, multi user : master 브랜치에서 다른 사람과 작업시 
      git stash
      git pull -r
      git stash pop
      git commit
      git push
      
#### Case2. Brach to branch : master에서 따온 내 작업 branch -> master branch
      git commit
      git chechout master
      git pull
      git merge
      git push

# 참고 URL
- https://backlog.com/git-tutorial/kr/stepup/stepup2_8.html
- https://git-scm.com/book/ko/v1/Git-%EB%B8%8C%EB%9E%9C%EC%B9%98-Rebase%ED%95%98%EA%B8%B0
- https://learngitbranching.js.org/?locale=ko
