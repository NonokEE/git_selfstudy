# 이전 상태 확인하기 실습 기록

## git show 결과
- HEAD version.txt 내용: `버전 3 내용입니다.`
- HEAD~1 version.txt 내용: `버전 2 내용입니다.`
- HEAD~2 version.txt 내용: `버전 1 내용입니다.`

## Detached HEAD 체험
- git checkout 실행 후 cat .git/HEAD 결과: `1f7a2bd424148a793e3263cbdc5708370d9e5aaa`
- 그 시점의 version.txt 내용: `버전 1 내용입니다.`
- git log --oneline 에서 HEAD 위치: `1f7a2bd (HEAD) practice: add version.txt v1`

## main 복귀 후 확인
- cat .git/HEAD 결과: `버전 3 내용입니다.`
- version.txt 내용: `ref: refs/heads/main`

## 새로 알게 된 점 또는 특이사항
- Detached HEAD 상태가 생각보다 유용하다. Detached 상태가 되면,
    ```Powershell
    Note: switching to '1f7a2bd'.

    You are in 'detached HEAD' state. You can look around, make experimental
    changes and commit them, and you can discard any commits you make in this
    state without impacting any branches by switching back to a branch.

    If you want to create a new branch to retain commits you create, you may
    do so (now or later) by using -c with the switch command. Example:

    git switch -c <new-branch-name>

    Or undo this operation with:

    git switch -

    Turn off this advice by setting config variable advice.detachedHead to false
    ```
    이런 식으로 친절하게 안내를 띄워준다.
    
    - detached 상태에서도 일단 얼마든지 커밋할 수 있다. 그리고 브랜치로 복귀하는 것 만으로, 이 상태에서 한 커밋들을 전부 버릴 수 있다.

    - detached 상태에서 커밋한 것들을 브랜치로 살리고 싶다면, switch에서 -c 옵션을 쓰면 된다.

    - 다시 브랜치로 돌아갈 때는, `git switch <브랜치명>`을 해도 되지만, `git switch - `를 해도 된다. 최근 브랜치로 돌아가는 듯?