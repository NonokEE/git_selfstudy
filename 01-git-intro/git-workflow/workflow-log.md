# Git 작업 흐름 실습

## 오늘 실습한 전체 흐름
1. git pull → Already up to date.
2. 파일 수정 → git-workflow/workflow-log.md 파일 추가 및 내용 작성
3. git add → 별도로 콘솔 출력은 없고, git status에서 표시되는내용이 Untracked files: 에서 Changes to be committed:로 변경됨
4. git commit → 커밋을 해야 메시지 확인을 하는데, 지금 커밋을 하면 커밋이 돼버리잖아.
5. git push → 이것도 마찬가지

## git status를 각 단계마다 확인한 결과
- pull 후: push를 해야 pull을 하고 확인을 하잖아
- add 전: Untracked files
- add 후: Changes to be committed
- commit 후: Your branch is ahead of 'origin/main' by 1 commit. (use "git push" to publish your local commits)