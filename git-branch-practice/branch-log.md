# 브랜치 실습 기록

### 브랜치 조회

```bash
git branch    # 브랜치 목록 표시
git branch -v # 브랜치 목록 + 각 브랜치 최신 커밋
```

```bash
git branch
---
  feature/hello
* main
```

```bash
git branch -v
  feature/hello 2d3c65f practice: initialize branch practice base file
* main          2d3c65f [ahead 1] practice: initialize branch practice base file
```

* main
이런식으로 * 붙은게 HEAD

### 브랜치 생성

```bash
git branch <브랜치이름>       # 새 브랜치 만들기 - 주의: 만들기만 하고 이동은 안함
git checkout -b <브랜치이름>  # 브랜치 만들면서 이동 / 이미 있으면 그냥 에러만 뜨고 암것도 안함
git switch -c <브랜치이름>    # 브랜치 만들면서 이동 / 이미 있으면 그냥 에러만 뜨고 암것도 안함
```

> 주의사항 : 만들기만 하는거지 이동은 안함.
> 

> 확인사항 : checkout -b나 switch -c 할 때 이미 있으면 `# fatal: a branch named 'feature/login' already exists` 뜨고 생성 안됨. 덮어쓰지도 않고 이동도 안함.
> 
> 
> 물론 예외는 있다.
> `checkout -B` 하거나 `switch -C` 하면 덮어쓰고 강제생성 할 수 있음.
> 기존에 있던 브랜치 커밋 내역은 다 날라감.
> 근데 쓸 일이 있나 이거, 테러용도 아니면.
> 

### 브랜치 삭제

```bash
git branch -d <브랜치이름>  # 안전 삭제(merge된 브랜치만 삭제. merge안된거 남아있으면 튕김)
git branch -D <브랜치이름>  # 강제 삭제(merge됐든 말든 지우라고)
```

> 주의사항1 : HEAD가 가리키고 있는 브랜치는 못 지움
주의사항2 : 지우기 전에 `git branch -v` 꼭 해라
> 

> 주의사항3 : 
merge안한 변경사항(commit 등)이 branch에 남아있으면 branch -d해도 튕긴다그랬잖아?
근데 그건 그 브랜치가 갈 곳이 없어서 그런건데, 갈 곳이 있으면 지울 수 있음
대표적인게 “remote”임…
그래서 publish 해버렸으면 거기로 간다 ㅋㅋ
> 

```bash
# 원격에 publish 안한 브랜치를 -d 옵션으로 제거
error: The branch 'feature/test' is not fully merged.
If you are sure you want to delete it, run 'git branch -D feature/test'.

# 원격에 publish 한 브랜치를 -d 옵션으로 제거
warning: deleting branch 'feature/bye' that has been merged to
         'refs/remotes/origin/feature/bye', but not yet merged to HEAD.
Deleted branch feature/bye (was 17ff94d).
```

### 브랜치 이동

```bash
git switch <브랜치이름>        # 이동
git switch -c <브랜치이름>     # 만들면서 이동
```

> 변경파일 커밋 안하고 이동하면???
그대로 싹 다 changes로 남아있음
충돌 주의
stash를 하든 임시로 commit을 하든 하셈.
>