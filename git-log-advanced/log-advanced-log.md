# git log 심화 실습 기록

## --oneline 결과
```Powershell
907f6ab (HEAD -> main) docs: add project description
a739900 fix: add bug fix log
c9473a0 feat: add automation script draft
eddfcf1 (origin/main, origin/HEAD) docs: update progress - 파일 삭제 및 이름 변경 추적 완료
... 중략 ...
a462a58 initial commit
a44f9c8 Initial commit
```

## --grep="practice" 결과
```Powershell
b3bae32 practice: ignore track-remove.txt via .gitignore
1943dc0 practice: add rm-mv practice log
98d999c practice: rename old-name.txt to new-name.txt using git mv
... 중략 ...
7649ff3 practice: add why Git is a DVCS
6c6ce4b practice: add version control concepts summary
77c72aa practice: summarize what Git is
```

## -- git-log-advanced/ 결과
```Powershell
commit 907f6abdda03f7ec30551d072383c7eecd7e821b (HEAD -> main)
Author: NonokEE <shshrdl@naver.com>
Date:   Tue Jun 23 21:45:53 2026 +0900

    docs: add project description

commit a7399003e665b1254ecd290f447952b6ecd644ef
Author: NonokEE <shshrdl@naver.com>
Date:   Tue Jun 23 21:45:24 2026 +0900

    fix: add bug fix log

commit c9473a094362da616e5a8fe3718aefe4def50a2f
Author: NonokEE <shshrdl@naver.com>
Date:   Tue Jun 23 21:44:50 2026 +0900

    feat: add automation script draft
```

## -S "버그 수정" 결과
```Powershell
commit a7399003e665b1254ecd290f447952b6ecd644ef
Author: NonokEE <shshrdl@naver.com>
Date:   Tue Jun 23 21:45:24 2026 +0900

    fix: add bug fix log
```

## 새로 알게 된 점 또는 특이사항
- 옵션이 정말 많다. 나중에 커밋로그 수천개씩 쌓이면 조회하는데도 시간 꽤 걸릴 것 같은데? 그런데 아마 브랜치별로 조회하는 옵션이 있지 않을까 싶음. 그때 가서 또 배우면 되지.
- -p -S "문자열" 이 옵션 조합도 상당히 유용할듯. 범인찾기 아주 좋아보인다.