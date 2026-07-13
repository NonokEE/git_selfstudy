# 협업 전 로컬 이력 정리 실습

## 실습 목표
- 지저분한 커밋을 의도적으로 생성
- git rebase -i 로 커밋 정리 (squash, reword)
- 정리 전후 git log 비교
```Powershell
# 정리 전
git log --oneline -5
###
826fe72 (HEAD -> feature/history-cleanup) typo fix2
9887e13 typo fix
6cbac8f wip: 일단 저장
10c4928 (origin/main, origin/HEAD, main) docs: update progress - 브랜치 정리와 이력 관리 습관 완료
c01995d docs: update cleanup-log.md
```
```Powershell
# 정리 후
###
practice: add local history cleanup exercise log
10c4928 (origin/main, origin/HEAD, main) docs: update progress - 브랜치 정리와 이력 관리 습관 완료
c01995d docs: update cleanup-log.md
b120ffb merge: integrate branch cleanup practice
6806625 practice: add branch cleanup exercise log
```

## 메모
- squash: 이전 커밋에 합치기
- fixup: 메시지 버리고 합치기
- reword: 메시지만 수정