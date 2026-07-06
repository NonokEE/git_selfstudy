# reflog 복구 실습 기록

## 체험한 시나리오
1. reset --hard HEAD~3 으로 커밋 3개 날림
2. git reflog 로 SHA 찾아서 복구 성공
3. git branch -D 로 브랜치 삭제
4. git reflog 로 SHA 찾아서 브랜치 복구 성공