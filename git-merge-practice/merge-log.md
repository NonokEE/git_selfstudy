# merge 실습 기록

## 12) 브랜치 병합 기초

git merge : 브랜치 합치는 명령어

### “합쳐질 대상”에서부터 다른 브랜치 끌어당겨서 합치는거임.

```bash
git switch main
git merge feature/login

이래야 [main <- feature/login]이 된다고.
```

대상 꼭꼭 조심해라

---

### Merge의 두 가지 방식

1. Fast-forward merge
    
    main에서 앞에 아무것도 없을 때.
    
    ```bash
    [merge 전]
    main:           A ── B
                          \
    feature/login:         C ── D
    
    ```
    
    ```bash
    [merge 후]
    main:           A ── B ── C ── D
                                    ↑
                                  HEAD
    ```
    
    그냥 다른 브랜치 끌어다가 붙이면 되는거라서 merge-commit 안생김.
    그냥 일직선 이력 유지됨
    
    ```bash
    git merge feature/ff-test 
    ---
    Updating 366a7a9..231b37d
    Fast-forward
     git-merge-practice/ff-feature.md | 1 +
     git-merge-practice/ff-feature2md | 1 +
     2 files changed, 2 insertions(+)
     create mode 100644 git-merge-practice/ff-feature.md
     create mode 100644 git-merge-practice/ff-feature2md
    ```
    
    이런식으로 로그 띄워서 fast-forward했다고 명시해준다.
    
    !image.png
    
    ```bash
    * 231b37d practice: add ff-feature2.md on feature/ff-test
    * c501482 practice: add ff-feature.md on feature/ff-test
    * 366a7a9 practice: initialize merge practice base file
    ```
    
    트리 봐도 이런식으로 feature/ff-test에서 썼던거 그대로 내려옴
    
2. merge commit (3-way merge)
    
    main에서도 뭔가 해놨을 때
    
    ```bash
    [merge 전]
    main:           A ── B ── E
                          \
    feature/login:         C ── D
    ```
    
    ```bash
    [merge 후]
    main:           A ── B ── E ── M (merge commit)
                          \       /
    feature/login:         C ── D
    ```
    
    어떤걸 어떻게 합쳐야할지 따져야하기 때문에 merge commit을 만들어야 함.
    그래프에서도 합쳐지는 모양을 볼 수 있다.
    
    - 하지만!!! ORT가 등장한다면 어떨까?
        
        Optimized Recursive Tree merge
        라는, git 2.34에 추가된 새로운 머지 방법임
        
        사실 이걸 얘기하려면 recursive merge를 먼저 얘기해야하는데 일단은 패스.
        ORT가 recursive merge보다 성능면에서 나은거라고 생각하면 됨
        
        지금 챕터에서 중요한 내용은,
        3-way merge의 조건이 되면, git에서 자체적으로 적절한 알고리즘을 판단한다는거다.
        그렇다고 그게 3-way merge가 아닌건 아님. 실제로 어떻게 동작할지에 대한 알고리즘이지.
        
        ```bash
        git merge feature/mc-test 
        ---
        Merge made by the 'ort' strategy.
         git-merge-practice/mc-feature.md | 1 +
         1 file changed, 1 insertion(+)
         create mode 100644 git-merge-practice/mc-feature.md
        ```
        
        로그는 이렇게 찍힘.
        3-way라는 명시가 없지만, ‘ort’ strategy를 사용했다고 하는 부분에서
        ”아 3-way를 했는데 ‘ort’라는 전략으로 했구나’라고 이해하면 된다.
        
        !image.png
        
        ```bash
        *   019bf92 (HEAD -> main) Merge branch 'feature/mc-test'
        |\  
        | * 0236405 (feature/mc-test) practice: add mc-feature.md on feature/mc-test
        * | 9a4b9b9 practice: update merge-log.md on main
        |/  
        * 231b37d practice: add ff-feature2.md on feature/ff-test
        ```
        
        그래프는 이렇게 그려진다.
        아무튼 일단 3-way merge가 실행되긴 한거임.
        

---

그래서 fastforward merge에서도 merge commit을 만들고 싶다면(3-way를 유도하고 싶다면)
분기 시점 이후에 일부러 main에다가 empty commit같은걸 남기는 것도 생각할 수 있을듯.

예를 들어, 특정 시점에서 3명이 각자 자기 업무 브랜치로 갈랐다고 할 때,
한 명이 먼저 merge하면 그 사람은 fast-forward, 나머지 두명은 3-way가 됨

근데 누가 한거든 merge commit 남기게 하고 싶다면,
분기 직후 시점에 main에다가 그냥 empy commit같은거 일부러 남겨서 3-way를 유도할 수 있을 듯.

---

### merge 후에 브랜치 어캐함?

보통은 지움 ㅇㅇ

```bash
git branch -d feature/login    # merge 완료됐으므로 -d로 안전하게 삭제 가능
```

이거 해도 그냥 잘 삭제될거임
branch가 내부 메타데이터로 자기가 안전하게 merge된 상태인지 아닌지 가지고 있기 때문이라고 함.

---

### 자주 하는 실수

- 현재 브랜치에서 다른 브랜치를 당겨오는거다.
main ← feature 하고 싶으면
switch main 해놔야한다고
- 브랜치 정리 안하면 나중에 보기 드러워집니다.
꼭꼭 범인을 찾아서 족칩시다.
- 컨플릭트 났다고 프로젝트 망하는거 아님. 천천히 풀면 됩니다.
물론 망할정도로 꼬일수도 있긴한데, 그건 그 지경되게 냅둔 리더 잘못 아닌지?