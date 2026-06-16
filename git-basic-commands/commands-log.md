# 기본 명령어 실습 기록

## git status
- 기본 출력: 
```PowerShell
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        git-basic-commands/
```
- -s 옵션 출력:
```PowerShell
?? git-basic-commands/
```
- 차이점: (직접 작성)

## git add
- 특정 파일만 add 후 git status -s 결과:
```PowerShell
A  git-basic-commands/file-a.md
?? git-basic-commands/commands-log.md
?? git-basic-commands/file-b.md
```
- git add . 후 git status -s 결과:
```PowerShell
# 커밋 순서 헷갈려서 이거만 나옴 ㅎㅎ 원래는 A file-a.md도 있어야함
A  git-basic-commands/commands-log.md
A  git-basic-commands/file-b.md
```

## git commit
- -m 옵션: 제일 많이 쓰는 유형인듯. commit message에서 body까지 적을 일은 많이 없으니까.
- -am 옵션 체험 결과: 보통 커밋할 때는 여러 파일 스테이지한 상태에서 하니까 쓸일이 많진 않을 것 같은데, 오탈자 수정같은 사소한거 할때는 그냥 간단하게 할 수 있을 듯. 그래도 커밋로그 너무 지저분해지니까 가급적이면 한번한번 커밋할 땐 신중하게 하는게 좋지 않을까 싶긴 함.

## git log
- --oneline 결과:
```PowerShell
cca0541 (HEAD -> main) practice: build template for observation log
7d693b0 practice: add basic commands exercise files
4bfa15f practice: add basic commands exercise files
a72598d (origin/main, origin/HEAD) docs: update progress - 파일 상태 이해
bdbbae2 practice: observe all four git file states
```
- --oneline --graph 결과:
```PowerShell
* cca0541 (HEAD -> main) practice: build template for observation log
* 7d693b0 practice: add basic commands exercise files
* 4bfa15f practice: add basic commands exercise files
* a72598d (origin/main, origin/HEAD) docs: update progress - 파일 상태 이해
* bdbbae2 practice: observe all four git file states
```
- 비교: 아직 브랜치가 없어서 그런가 뚜렷한 차이는 없다.
