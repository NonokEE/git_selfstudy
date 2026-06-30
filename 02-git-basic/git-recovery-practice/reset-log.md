## reset

```bash
git reset --soft HEAD~n    # 헤드에서 1번째로 떨어진 커밋으로 시점 이동

git reset HEAD~n           # reset의 기본값은 --mixed
git reset --mixed HEAD~n
```

HEAD를 특정 커밋으로 되돌린다.
restore는 단순히 파일만 복구했는데, **reset은 커밋 이력 자체를 조작해버린다.**
그래서 옵션에 따라 파일의 최종 상태도 바뀌어버릴 수 있음.

[Working Directory]  ←→  [Staging Area]  ←→  [Repository (커밋)]
이 구조 기억하지?

### `git reset --soft`

HEAD만 되돌리고, staging area랑 working directory는 유지한다.
즉, 커밋로그를 그지같이 찍어서 취소하고 싶은데, 변경 내용은 냅두고 다시 이쁘게 커밋하고 싶을 때 쓴다.

> 주의 : git reset --soft HEAD ← 이걸로 잘못치면 뭔가 이상해짐. 이후 HEAD~1이 이상하게 적용돼.
이유는 모르겠는데, 암튼 조심
> 

> 주의 : graph에서 헤드 위치 잘 보셈 ㅋㅋㅋㅋ
outgoing changes는 push할게 남았다는 뜻이고,
내 local head는 main임
remote head는 origin/main이고
> 

### `git reset --mixed`(기본값)

HEAD랑 Staging Area를 되돌리고, Working Directory는 유지
restore --staged . 하고 git reset --soft 하면 git reset --mixed랑 다를게 없음

mixed가 기본값이라서, git reset HEAD~1 이런거 하면 --mixed로 인식됨

### git reset --hard

진짜 다 날리고 HEAD를 되돌림.
근데 여기까지만. 나중에 revert 차이 설명할 때 다시 오겠노라

### 결론

1. 수정은 하고 싶은데 쫄리면 reset --soft하거나 --mixed해라
2. 파일들은 다 내가 작업한, 의미있는게 맞는데, commit 로그들만 수정하고 싶은거면 soft/mixed
    
    개인적으로는 mixed를 하는게 맞는거 같음. 굳이 soft를 할 이유가 없다.
    스테이징 정도는 다시 하면 되는거니까. 
    reset soft나 mixed를 하는 이유를 생각해보면, 우선 mixed로 하고, 어떤거 stage할지 다시 정하는게 맞을 것 같음
    
3. 파일 자체를 잘못 올려서, 진짜 날려버리는게 확실하면 hard일 것으로 추정. 실수로 우리집 강아지 사진을 넣은걸 commit 해버렸다든지.