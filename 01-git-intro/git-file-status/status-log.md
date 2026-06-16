# 파일 상태 이해 실습

## 오늘 배운 4가지 상태

### 1. Untracked
- git status 출력:
```bash
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        git-file-status/
```

### 2. Staged
- git add 후 git status 출력:
```bash
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   git-file-status/status-log.md
```

### 3. Unmodified
- git commit 후 git status 출력:
```bash
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

### 4. Modified
- 파일 수정 후 git status 출력:
```bash
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   git-file-status/status-log.md
```

## Staged + Modified 동시 발생
- 상황:
    1. status-log.md 파일을 stage한 상태에서
    2. status-log.md 파일 수정(not staged)
- git status 출력:
```bash
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   git-file-status/status-log.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   git-file-status/status-log.md
```
