# GitTestRepo

Testing Git strategy for environmental branching. 

https://www.wearefine.com/mingle/env-branching-with-git/


Create topic branch
git checkout master
git pull origin master
git checkout -b topic-branch

Create Pull Request into Development
git checkout topic-branch
git pull --rebase origin Development
git push origin topic-branch
(create PR for Development)

Merge to Staging (release)
# checkout your feature branch and rebase from master
git checkout topic-branch
git pull --rebase origin master
 git checkout stage
git pull --rebase origin stage
git merge topic-branch
git push origin stage

Merge to Master (production)
git checkout topic-branch
git pull --rebase origin master
git push origin topic-branch
Git checkout master
Git merge topic-branch
Git push origin master 
