# Git 설치 및 환경 확인

## git --version 실행 결과
git version 2.34.1.windows.1

## git config user.name 실행 결과
NonokEE

## git config user.email 실행 결과
shshrdl@naver.com

## git config --list 실행 결과
diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
http.sslbackend=openssl
http.sslcainfo=C:/Program Files/Git/mingw64/ssl/certs/ca-bundle.crt
core.autocrlf=true
core.fscache=true
core.symlinks=false
pull.rebase=false
credential.helper=manager-core
credential.https://dev.azure.com.usehttppath=true
init.defaultbranch=master
user.email=shshrdl@naver.com
user.name=NonokEE
core.longpaths=true
core.editor="C:\Users\Master\AppData\Local\Programs\Microsoft VS Code\bin\code" --wait
difftool.sourcetree.cmd='' "$LOCAL" "$REMOTE"
mergetool.sourcetree.cmd=''
mergetool.sourcetree.trustexitcode=true
init.defaultbranch=main
core.repositoryformatversion=0
core.filemode=false
core.bare=false
core.logallrefupdates=true
core.symlinks=false
core.ignorecase=true
remote.origin.url=https://github.com/NonokEE/git_selfstudy.git
remote.origin.fetch=+refs/heads/*:refs/remotes/origin/*
branch.main.remote=origin
branch.main.merge=refs/heads/main
branch.main.vscode-merge-base=origin/main

## config 레벨 정리 (본인 말로)
- system: 컴퓨터 전체 범위
- global: user 범위
- local: 프로젝트 범위

## 오늘 새로 알게 된 점
- git config에 scope가 있는 줄 몰랐음
- 컴퓨터에 처음 git 깔고 commit 할 때, 웬 name이랑 email 적으라고 하던게 이거구나