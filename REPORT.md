№1
git checkout ci
git rebase -i HEAD~2
git checkout master
git cherry-pick ci
git branch -D ci

№2
git reflog
git checkout aca3abb
git branch old-master

№3
git blame -L 32,32 prisma/seed.ts