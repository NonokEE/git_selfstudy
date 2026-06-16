# 첫 Git 저장소 만들기 실습

## 실습한 명령어와 결과
- git init 결과:
```bash
Initialized empty Git repository in C:/Users/Master/Desktop/Nonok_git/my-first-repo/.git/
```
- git remote add 결과: 터미널에 별도 출력은 없고, "origin"이라는 이름으로 원격 생성됨
- git remote -v 결과: 
```bash
git remote -v :
origin  https://github.com/NonokEE/my-first-repo.git (fetch)
origin  https://github.com/NonokEE/my-first-repo.git (push)
```
- git push -u 결과:
```bash
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 417 bytes | 417.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/NonokEE/my-first-repo.git
* [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
```

## 새로 알게 된 것
- CLI 안익숙한 애기들ㄹ이 git init을 홈 디렉토리에서 해버릴 수도 있다는거? 남들 알려줄 때 좀 신경써야겠다.
