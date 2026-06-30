# 파일 수정 이력 확인 실습 요약

## 사용한 명령어
- `git log --oneline -- log-test.txt` : 파일 관련 커밋만 필터링
- `git diff --staged` : add 후 변경사항 확인
- `git blame log-test.txt` : 줄별 작성자 및 커밋 확인

## 느낀 점
CLI에서 보려니 진짜 보기 나쁘다. 그럴 일은 거의 없긴 하겠지.

git blame이거 드립으로만 봤는데, 이런 뜻이었구나. 작명 의도는 둘째치고, 일단 비난할 때 쓰긴 좋아보인다.
