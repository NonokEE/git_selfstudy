# 학습진행상황

## 기본 정보
- **학습 주제**: Git & GitHub
- **학습 순서**: Git 입문 → Git 초급 → Git 중급 → GitHub 입문 → GitHub 초급 → Git 고급 → GitHub 중급 → GitHub 고급
- **현재 상태**: 진행 중
- **학습 시작일**: 2026-06-12

---

## 전체 로드맵
- [x] Git 입문
- [x] Git 초급
- [x] Git 중급
- [ ] GitHub 입문
- [ ] GitHub 초급
- [ ] Git 고급
- [ ] GitHub 중급
- [ ] GitHub 고급

---

## 진행 기록 작성 템플릿

<details>
<summary>기록 형식 보기</summary>

```markdown
### [세부 목차명]
- 상태: 시작 전 / 진행 중 / 완료
- 이론 완료일: YYYY-MM-DD
- 실습 완료일: YYYY-MM-DD
- 관련 커밋/PR/폴더: 
```

예시:

```markdown
### Git이란 무엇인가
- 상태: 완료
- 이론 완료일: 2026-06-11
- 실습 완료일: 2026-06-11
- 관련 커밋/PR/폴더: docs/git-intro/
- 비고: working directory, staging area, repository 개념을 구분하는 데 시간이 조금 걸렸음.
```

</details>

---

## 진행 기록

### Git

<details>
<summary>Git 입문</summary>

#### 저장소 개요
- 단계 상태: 완료 ✅
- 이론 완료: ✅
- 실습 완료: ✅

### Git이란 무엇인가
- 상태: 완료
- 이론 완료일: 2026-06-12
- 실습 완료일: 2026-06-12
- 관련 커밋/PR/폴더: git-intro/what-is-git.md
- 비고: Git의 정의, 필요성, Git vs GitHub 개념 학습 

### 버전 관리의 개념
- 상태: 완료
- 이론 완료일: 2026-06-15
- 실습 완료일: 2026-06-15
- 관련 커밋/PR/폴더: git-intro/version-control.md
- 비고: 로컬/CVCS/DVCS 3가지 유형 비교, Git이 DVCS인 이유 학습

### Git을 사용하는 이유
- 상태: 완료
- 이론 완료일: 2026-06-15
- 실습 완료일: 2026-06-15
- 관련 커밋/PR/폴더: git-intro/why-git.md
- 비고: VCS 관점에서 Git의 위치를 이해함. 버전 관리, 백업, 협업의 세 가지 측면에서 Git의 필요성을 정리함

### 로컬 저장소와 원격 저장소의 차이
- 상태: 완료
- 이론 완료일: 2026-06-15
- 실습 완료일: 2026-06-15
- 관련 커밋/PR/폴더: git-intro/local-vs-remote.md
- 비고: git remote -v 명령어로 원격 저장소 연결 확인. fetch/push 주소의 의미 학습

### Git 설치 및 환경 확인
- 상태: 완료
- 이론 완료일: 2026-06-15
- 실습 완료일: 2026-06-15
- 관련 커밋/PR/폴더: git-intro/git-environment.md
- 비고: git config --list로 환경 확인. config 레벨(system/global/local) 우선순위 이해. 같은 항목이 두 레벨에 있을 때 local이 우선 적용됨을 확인

### Git 초기 설정
- 상태: 완료
- 이론 완료일: 2026-06-15
- 실습 완료일: 2026-06-15
- 관련 커밋/PR/폴더: git-intro/git-config.md
- 비고: user.name/email/init.defaultBranch/core.autocrlf 설정 완료. Windows 환경이므로 autocrlf=true 적용. core.editor=code --wait 설정 확인

### 저장소(repository)의 개념
- 상태: 완료
- 이론 완료일: 2026-06-16
- 실습 완료일: 2026-06-16
- 관련 커밋/PR/폴더: git-repo-concept/repo-concept.md
- 비고: Working Directory → Staging Area → Repository 세 가지 영역 흐름 체험. git init 시 .git 폴더 생성 확인. 서브모듈 문제 경험 및 해결

### Git 작업 흐름 개요
- 상태: 완료
- 이론 완료일: 2026-06-16
- 실습 완료일: 2026-06-16
- 관련 커밋/PR/폴더: git-workflow/workflow-log.md
- 비고: pull→add→commit→push 전체 사이클 체험. commit 후 "ahead of origin/main by 1 commit" 메시지 직접 확인. 각 단계 터미널 출력 메시지가 곧 결과임을 인지

### 첫 Git 저장소 만들기
- 상태: 완료
- 이론 완료일: 2026-06-16
- 실습 완료일: 2026-06-16
- 관련 커밋/PR/폴더: git-first-repo/first-repo-log.md
- 비고: git init → remote add → push -u 전체 흐름 체험. -u 옵션으로 upstream 설정 확인. git remote add는 성공 시 출력 없음 확인

### 파일 상태 이해
- 상태: 완료
- 이론 완료일: 2026-06-16
- 실습 완료일: 2026-06-16
- 관련 커밋/PR/폴더: git-file-status/status-log.md
- 비고: Untracked→Staged→Unmodified→Modified 4가지 상태 직접 체험. 동일 파일이 Staged+Modified에 동시 표시되는 상황도 재현 성공

### 기본 명령어 익히기
- 상태: 완료
- 이론 완료일: 2026-06-16
- 실습 완료일: 2026-06-17
- 관련 커밋/PR/폴더: git-basic-commands/commands-log.md
- 비고: status/add/commit/log 주요 옵션 체험. -s 옵션으로 간결한 상태 확인, --graph는 브랜치 생기면 진가 발휘 예정. -am은 사소한 수정에 유용하나 신중히 사용할 것

</details>

<details>
<summary>Git 초급</summary>

#### 저장소 개요
- 단계 상태: 완료 ✅
- 이론 완료: ✅
- 실습 완료: ✅

### 커밋(commit)의 의미와 좋은 커밋 습관
- 상태: 완료
- 이론 완료일: 2026-06-17
- 실습 완료일: 2026-06-17
- 관련 커밋/PR/폴더: git-commit-practice/
- 비고: Conventional Commits 스타일(type: 설명) 적용. 하나의 목적 = 하나의 커밋 원칙 체험. project-info.md, todo.md를 각각 별도 커밋으로 분리 성공

### 여러 파일 추가 및 선택적 스테이징
- 상태: 완료
- 이론 완료일: 2026-06-17
- 실습 완료일: 2026-06-17
- 관련 커밋/PR/폴더: git-staging-practice/
- 비고: git add 파일 단위 선택, git restore --staged로 unstage 체험. git status -su로 untracked 파일 상세 확인 방법 추가 학습

### 파일 수정 이력 확인
- 상태: 완료
- 이론 완료일: 2026-06-22
- 실습 완료일: 2026-06-22
- 관련 커밋/PR/폴더: git-log-practice/
- 비고: git log --, git diff, git diff --staged, git blame 명령어 체험. CLI 출력이 불편할 때 GUI 도구(GitLens 등) 활용 가능함을 인지.

### 파일 삭제 및 이름 변경 추적
- 상태: 완료
- 이론 완료일: 2026-06-23
- 실습 완료일: 2026-06-23
- 관련 커밋/PR/폴더: git-rm-mv-practice/
- 비고: git rm / git rm --cached / git mv 세 가지 명령어 체험. --cached 사용 시 D + ?? 동시 표시되는 원리 스스로 분석 성공. untracked 파일은 .gitignore에 등록하여 깔끔하게 마무리.

### 커밋 기록 조회 심화
- 상태: 완료
- 이론 완료일: 2026-06-23
- 실습 완료일: 2026-06-23
- 관련 커밋/PR/폴더: git-log-advanced/
- 비고: --oneline / --grep / --author / -- 경로 / -S 옵션 체험. -p -S 조합으로 코드 변경 추적 가능함을 인지. 브랜치별 로그 조회는 브랜치 학습 시 연계 예정.

### HEAD의 개념
- 상태: 완료
- 이론 완료일: 2026-06-23
- 실습 완료일: 2026-06-23
- 관련 커밋/PR/폴더: git-head-practice/
- 비고: HEAD → 브랜치 → 커밋 구조 이해. .git/HEAD 파일 직접 확인. HEAD~n 상대 참조로 이전 커밋 SHA 대조 완료. Detached HEAD는 이전 상태 확인하기에서 연계 예정.

### 이전 상태 확인하기
- 상태: 완료
- 이론 완료일: 2026-06-23
- 실습 완료일: 2026-06-23
- 관련 커밋/PR/폴더: git-checkout-practice/
- 비고: git show HEAD~n:경로 로 파일 내용 읽기 성공. Detached HEAD 직접 체험 및 .git/HEAD에 SHA 직접 출력 확인. git switch - 단축 명령어 및 -c 옵션으로 새 브랜치 생성 가능함을 자체 파악.

### .gitignore의 역할과 작성법
- 상태: 완료
- 이론 완료일: 2026-06-24
- 실습 완료일: 2026-06-24
- 관련 커밋/PR/폴더: git-gitignore-practice/
- 비고: 패턴 규칙(*, /, !) 학습. --cached로 이미 추적 중인 파일 제외 체험. .gitignore 적용 파일에 -f 강제 추가 vs advice 메시지 비활성화의 차이 자체 분석 성공.

### 실수 복구 기초
- 상태: 완료
- 이론 완료일: 2026-06-30
- 실습 완료일: 2026-06-30
- 관련 커밋/PR/폴더: git-recovery-practice/
- 비고: git restore / git restore --staged / git commit --amend 체험 (1차).
  git reset --soft / --mixed 보충 학습 (2차).
  restore --staged + reset --soft = reset --mixed 관계 스스로 도출.
  --hard는 Git 중급 reset vs revert 단계에서 연계 예정.

### 브랜치(branch)의 개념
- 상태: 완료
- 이론 완료일: 2026-06-30
- 실습 완료일: 2026-06-30
- 관련 커밋/PR/폴더: git-branch-practice/
- 비고: 브랜치는 커밋을 가리키는 포인터임을 이해. 실습은 다음 챕터와 통합 진행.

### 브랜치 생성, 이동, 삭제
- 상태: 완료
- 이론 완료일: 2026-06-30
- 실습 완료일: 2026-06-30
- 관련 커밋/PR/폴더: git-branch-practice/
- 비고: branch/switch -c/branch -d/-D 체험. -d는 merge 여부가 아닌 커밋 보존 여부를 확인함을 직접 발견.
  원격 publish 여부에 따라 -d 결과가 달라지는 원리 자체 분석 성공.
  커밋 안 하고 브랜치 이동 시 변경사항이 따라오는 현상도 자체 발견.

### 브랜치 병합 기초
- 상태: 완료
- 이론 완료일: 2026-07-01
- 실습 완료일: 2026-07-01
- 관련 커밋/PR/폴더: git-merge-practice/
- 비고: fast-forward / 3-way merge 두 케이스 직접 체험.
  ORT strategy는 3-way 여부와 별개로 계산 알고리즘임을 자체 분석 성공.
  empty commit으로 3-way 유도 아이디어 도출 → --no-ff 옵션으로 더 깔끔하게 해결 가능함을 추가 학습.

### fast-forward merge와 merge commit의 차이
- 상태: 완료
- 이론 완료일: 2026-07-01
- 실습 완료일: 2026-07-01
- 관련 커밋/PR/폴더: git-merge-practice/
- 비고: 이전 브랜치 병합 기초 실습에서 이미 체험 완료.
  --no-ff로 fast-forward 강제 차단, --ff-only로 fast-forward만 허용하는 옵션 추가 학습.

### 충돌(conflict)의 개념과 기본 해결 절차
- 상태: 완료
- 이론 완료일: 2026-07-01
- 실습 완료일: 2026-07-01
- 관련 커밋/PR/폴더: git-conflict-practice/
- 비고: CLI 마커 직접 편집 + VS Code GUI 버튼 방식 두 가지 체험.
  마커를 남긴 채 커밋 가능하지만 코드가 망가짐을 자체 발견.
  merge --abort로 충돌 전 상태 복구 체험.
  충돌 예방은 협업 정책과 인터페이스 설계가 핵심임을 스스로 도출.

</details>

<details>
<summary>Git 중급</summary>

#### 저장소 개요
- 단계 상태: 완료 ✅
- 이론 완료: ✅
- 실습 완료: ✅

### 브랜치 전략 기초
- 상태: 완료
- 이론 완료일: 2026-07-04
- 실습 완료일: 2026-07-04
- 관련 커밋/PR/폴더: git-branch-strategy/strategy-log.md
- 비고: GitHub Flow / Git Flow / Trunk-based 3가지 전략 개념 학습.
  브랜치 네이밍 규칙(feature/, fix/, hotfix/) 적용 체험.
  feature 브랜치 → main merge 시 fast-forward 발생 원리 스스로 파악.
  실제 GitHub Flow에서는 PR을 통해 merge하는 것이 정석임을 인지.

### merge와 rebase의 차이
- 상태: 완료
- 이론 완료일: 2026-07-05
- 실습 완료일: 2026-07-05
- 관련 커밋/PR/폴더: git-rebase-practice/merge-log.md
- 비고: merge = 현재 브랜치가 대상 브랜치를 흡수, merge commit 생성.
  rebase = base를 옮기는 것, 브랜치 합치기 아님 → 이후 ff merge 필요.
  rebase 후 committer date 변경으로 SHA 재생성 직접 확인.
  공유된 브랜치(dev 등) rebase 시 팀원 이력 전체가 꼬이는 원리 자체 분석 성공.

### rebase 사용법과 주의점
- 상태: 완료
- 이론 완료일: 2026-07-05
- 실습 완료일: 2026-07-05
- 관련 커밋/PR/폴더: git-rebase-advanced/rebase-practice.md
- 비고: main이 앞서간 상황에서 feature 브랜치 rebase 최신화 체험.
  rebase 후 author date ≠ committer date로 SHA 재생성 직접 확인.
  push 거부 → --force-with-lease로 안전한 강제 push 체험.
  merge commit 없는 일직선 이력 완성 확인.

### cherry-pick의 개념과 활용
- 상태: 완료
- 이론 완료일: 2026-07-05
- 실습 완료일: 2026-07-05
- 관련 커밋/PR/폴더: git-cherrypick-practice/
- 비고: cherry-pick은 커밋을 이동이 아닌 복사함을 이해.
  루트 저장소 내 실습이므로 git init 생략 (서브모듈 방지).
  feature 파일이 함께 올라간 것은 브랜치 전환 없이 진행된 구조적 특성.
  실제 독립 저장소에서는 main 브랜치에 bugfix.md만 남는 결과 확인 예정.

### 특정 커밋 되돌리기
- 상태: 완료
- 이론 완료일: 2026-07-05
- 실습 완료일: 2026-07-05
- 관련 커밋/PR/폴더: git-revert-practice/
- 비고: git revert = 되돌리는 새 커밋 생성, 이력 보존 → 공유 브랜치에 안전.
  충돌 발생 시 어느 쪽을 선택하느냐가 revert의 실제 효과를 결정함.
  최신 커밋(HEAD) 내용으로 해결하면 변경사항 없음 → revert 커밋 미생성.
  근본 원인은 커밋 분리 미흡 → 하나의 목적 = 하나의 커밋 원칙이 핵심.

### reset과 revert의 차이
- 상태: 완료
- 이론 완료일: 2026-07-05
- 실습 완료일: 2026-07-05
- 관련 커밋/PR/폴더: git-reset-practice/
- 비고: reset = HEAD를 되돌림(이후 커밋 전부 사라짐), revert = 취소 커밋 생성(이력 유지).
  --soft(staged 유지) / --mixed(unstaged 유지) / --hard(전부 삭제) 3가지 모드 체험.
  중간 커밋 하나만 없애려면 반드시 revert 사용. reset은 그 시점 이후 전부 날아감.
  push된 커밋에 reset 절대 금지 → revert가 정석.

### stash 활용
- 상태: 완료
- 이론 완료일: 2026-07-06
- 실습 완료일: 2026-07-06
- 관련 커밋/PR/폴더: git-stash-practice/
- 비고: 브랜치 전환 시 충돌 없으면 변경사항이 따라옴 → stash로 먼저 치우는 습관 필요.
  PowerShell에서 stash@{1} 문법 오작동 → 숫자 인덱스(git stash apply 1) 사용 권장.
  apply(목록 유지) vs pop(목록 삭제) 차이 체험. -u 옵션으로 untracked 파일 포함 저장 확인.

### 태그(tag) 관리
- 상태: 완료
- 이론 완료일: 2026-07-06
- 실습 완료일: 2026-07-06
- 관련 커밋/PR/폴더: git-tag-practice/
- 비고: lightweight(이름만) vs annotated(작성자·날짜·메시지 포함) 차이 체험.
  태그는 git push에 자동 포함 안 됨 → git push origin --tags 별도 필요.
  태그로 checkout 시 Detached HEAD 발생. 변경사항 없으면 불필요한 커밋 생략.

### 로그 탐색 심화
- 상태: 완료
- 이론 완료일: 2026-07-06
- 실습 완료일: 2026-07-06
- 관련 커밋/PR/폴더: git-log-advanced2/
- 비고: --grep(메시지) vs -S(코드 내용) 차이 학습.
  main..feature(단방향) vs main...feature(양방향) 점 개수 차이 체험.
  --pretty=format으로 커스텀 출력 포맷 적용 확인.

### Git 내부 객체 개요
- 상태: 완료
- 이론 완료일: 2026-07-06
- 실습 완료일: 2026-07-06
- 관련 커밋/PR/폴더: git-log-advanced2/git-objects-log.md
- 비고: blob/tree/commit/tag 4가지 객체 구조 이해.
  git cat-file -t / -p 로 객체 타입과 내용 직접 확인.
  수정되지 않은 파일의 blob SHA는 커밋이 달라도 동일함(재사용) 직접 확인.
  변경된 경로 위쪽 tree만 새로 생성되는 원리, 형상 관리에 삭제 연산이 없는 이유 자체 도출.

### reflog의 개념과 복구
- 상태: 완료
- 이론 완료일: 2026-07-06
- 실습 완료일: 2026-07-07
- 관련 커밋/PR/폴더: git-log-advanced2/reflog-practice.md
- 비고: reset --hard 복구, 브랜치 삭제 복구 두 시나리오 직접 체험.
  reflog SHA는 "HEAD가 가리키던 커밋"이지 브랜치 말단이 아님을 자체 분석.
  git reflog show <브랜치명>이 올바른 브랜치 복구 방법임을 스스로 도출.
  gc --prune과 형상 관리 철학의 차이까지 자체 정리 완료.

### 브랜치 정리와 이력 관리 습관
- 상태: 완료
- 이론 완료일: 2026-07-10
- 실습 완료일: 2026-07-13
- 관련 커밋/PR/폴더: git-branch-cleanup-practice/cleanup-log.md
- 비고: feature 브랜치 생성 → 병합 → 로컬 삭제 → fetch --prune 전체 흐름 체험.
  git fetch --prune을 pull처럼 습관화할 것. fetch.prune true 전역 설정으로 자동화 가능.
  --no-ff merge로 병합 지점을 이력에 명시적으로 남기는 방식 적용.

### 협업 전 로컬 이력 정리 기본기
- 상태: 완료
- 이론 완료일: 2026-07-13
- 실습 완료일: 2026-07-13
- 관련 커밋/PR/폴더: git-history-cleanup-practice/history-cleanup-log.md
- 비고: wip/typo 커밋 3개를 rebase -i로 하나로 squash(fixup) 체험.
  정리 전후 git log를 파일에 직접 기록해 비교 확인.
  rebase 후 추가 수정은 --amend로 이전 커밋에 합치는 습관이 더 깔끔함을 인지.
  핵심 원칙: push 전에 정리하고, push 후에는 바꾸지 않는다.

</details>

<details>
<summary>Git 고급</summary>

#### 저장소 개요
- 단계 상태: 시작 전
- 이론 완료: ⬜
- 실습 완료: ⬜

### Git 내부 동작 원리 심화
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### detached HEAD 상태 이해
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### interactive rebase 활용
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### bisect를 이용한 문제 커밋 찾기
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 고급 복구 시나리오
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 서브모듈(submodule) 개요
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### worktree 개요
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 대형 프로젝트에서의 브랜치 운영 전략
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 커밋 메시지 규칙 설계
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 충돌 최소화를 위한 작업 방식
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### Git hooks 개요
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 성능 및 저장소 관리 기초
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 실제 현업에서 자주 발생하는 Git 문제 사례와 대응
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 안전한 이력 수정 원칙
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

</details>

### GitHub

<details>
<summary>GitHub 입문</summary>

#### 저장소 개요
- 단계 상태: 시작 전
- 이론 완료: ⬜
- 실습 완료: ⬜

### Git과 GitHub의 차이
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### GitHub 계정과 저장소 개념
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 공개 저장소와 비공개 저장소의 차이
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### GitHub 저장소 생성하기
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 로컬 Git 저장소와 GitHub 연결하기
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 원격 저장소 개념
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 기본 원격 작업
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### README.md 작성 기초
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 원격 저장소 복제하기
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### GitHub 웹 화면 기본 구조 이해
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 기본 마크다운 문법
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 첫 번째 GitHub 업로드 실습 흐름 이해
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

</details>

<details>
<summary>GitHub 초급</summary>

#### 저장소 개요
- 단계 상태: 시작 전
- 이론 완료: ⬜
- 실습 완료: ⬜

### 브랜치를 활용한 GitHub 작업 흐름
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### Pull Request(PR)의 개념
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### Pull Request 생성 및 검토 기초
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 코드 리뷰 기본 예절
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### merge 방식 이해
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### Issues 사용법
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### Issue와 커밋/PR 연결하기
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### Labels, Assignees, Milestones 기초
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### Fork의 개념
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### Fork 기반 협업 흐름 기초
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### upstream 저장소와 동기화
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### GitHub에서 충돌 확인 및 해결 흐름
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### Releases 개념
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 프로젝트 소개 문서 정리
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

</details>

<details>
<summary>GitHub 중급</summary>

#### 저장소 개요
- 단계 상태: 시작 전
- 이론 완료: ⬜
- 실습 완료: ⬜

### 협업 중심 브랜치 전략 실전 적용
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### Pull Request 템플릿 만들기
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### Issue 템플릿 만들기
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### CODEOWNERS 개요
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### Discussions 기능 이해
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### Projects 기능 기초
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### Wiki 기능 개요
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### GitHub Actions 입문
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 간단한 CI 구성 예시
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 배지(badge) 활용
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 보호 브랜치(branch protection) 이해
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 리뷰 승인 정책 개요
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 권한과 역할 관리 기초
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 오픈소스 기여 기본 흐름
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

</details>

<details>
<summary>GitHub 고급</summary>

#### 저장소 개요
- 단계 상태: 시작 전
- 이론 완료: ⬜
- 실습 완료: ⬜

### GitHub Actions 심화
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 조직(Organization) 단위 협업 구조 이해
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 팀(Team) 권한 관리
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### Secrets와 환경 변수 관리
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### GitHub Pages 개요
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 패키지 배포 개요
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 보안 기능 개요
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 대규모 협업 프로젝트 운영 패턴
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### PR 리뷰 정책 설계
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### Issue/PR 자동화 전략
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 프로젝트 보드 운영 전략
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 릴리스 관리와 버전 정책
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 오픈소스 저장소 운영 모범 사례
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

### 포트폴리오용 GitHub 프로필/저장소 정리 전략
- 상태: 시작 전
- 이론 완료일: 
- 실습 완료일: 
- 관련 커밋/PR/폴더: 

</details>
