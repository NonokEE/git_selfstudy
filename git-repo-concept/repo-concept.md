# 저장소(Repository) 개념 실습

## .git 폴더 확인
- `git init` 실행 후 생성된 항목: ./git-repoconcept/.git 생성됨

## 세 가지 영역 체험
- Working Directory: 파일 생성 후 git status 결과 → [Untracked files] 영역에 repo-concept.md
- Staging Area: git add 후 git status 결과 → [Changes to be committed] 영역에 new file : repo-concept.md
- Repository: git commit 후 git status 결과 → nothing to commit, working tree clean

## 느낀 점
- source tree나 vscode ui로는 많이 봤는데 CLI로 보니까 또 신선하네