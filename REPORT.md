# REPORT для отчета по дев-тулзам
> Скрины в docs
---
## Task 1
GitKraken used

## Task 2
    git checkout ci
    git rebase -i HEAD~2
    git checkout master
    git cherry-pick ci
    git branch -D ci

## Task 3
    git reflog
    git checkout aca3abb
    git branch old-master

## Task 4
    git blame -L 32,32 prisma/seed.ts

## Task 5
    git checkout master
    git bisect start
    git bisect bad
    git bisect good 8673a6
    npm run test
    
    3c82961d432a69ff82d5fc958b841a54cb4c6234 is the first bad commit
    commit 3c82961d432a69ff82d5fc958b841a54cb4c6234
    Author: Nikolay Andreev <bakasaru@list.ru>
    Date:   Mon Dec 20 00:28:11 2021 +0300
    
    feat: add seed to get games from eShop API
    
    prisma/seed.ts     | 57 ++++++++++++++++++++++++++++++++++++++++++++++++++++++
    src/app.service.ts |  2 +-
    2 files changed, 58 insertions(+), 1 deletion(-)
    create mode 100644 prisma/seed.ts

## Task 6
    git filter-branch --tree-filter "rm -f .env" -- --all
    echo .env >> .gitignore

## Task 7
    git checkout feature
    git filter-branch --env-filter "GIT_AUTHOR_NAME='Арсентьев Даниил Геннадьевич';     GIT_AUTHOR_EMAIL='arsentev.danil2@mail.ru'; GIT_COMMITTER_NAME='Арсентьев Даниил Геннадьевич';     GIT_COMMITTER_EMAIL='arsentev.danil2@mail.ru'" HEAD~6..HEAD

## Task 8
    git checkout master
    git config rerere.enabled true
    git merge feature
    
    git commit -a --no-edit
    git reset --hard HEAD~1
    git merge feature
    
    git commit -a --no-edit

## Task 9
    git fsck

## Task 10
    git gc --prune=now --aggressive

## FOR THIS FILE
    git add -p
    e