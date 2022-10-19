№1
git checkout ci
git rebase -i HEAD~2
git checkout master
git cherry-pick ci
git branch -D ci