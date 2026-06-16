# Git 초기 설정 실습

## 적용한 설정 목록

| 설정 키 | 설정 값 | 설명 |
|---------|---------|------|
| user.name | NonokEE| 커밋에 기록될 이름 |
| user.email | shshrdl@naver.com | 커밋에 기록될 이메일 |
| init.defaultBranch | main | 기본 브랜치 이름 |
| core.autocrlf | true | 줄바꿈 처리 방식 |

## 설정 확인 명령어

```bash
git config --list --show-origin
###
file:C:/Users/Master/.gitconfig user.email=shshrdl@naver.com
file:C:/Users/Master/.gitconfig user.name=NonokEE
file:C:/Users/Master/.gitconfig core.longpaths=true
file:C:/Users/Master/.gitconfig core.editor=code --wait
file:C:/Users/Master/.gitconfig core.autocrlf=true
file:C:/Users/Master/.gitconfig difftool.sourcetree.cmd='' "$LOCAL" "$REMOTE"
file:C:/Users/Master/.gitconfig mergetool.sourcetree.cmd=''
file:C:/Users/Master/.gitconfig mergetool.sourcetree.trustexitcode=true
file:C:/Users/Master/.gitconfig init.defaultbranch=main
```

## 느낀 점 / 메모

- 이메일 지정하는거 gitHub랑 맞춰야되는구나 (정확히는 안맞춰도 되지만, contribute 추적이 안됨)
- 에디터 vim 안써도 되는구나 바꿀 수 있구나
- CRLF / LF - 이거 배웠음
- git config에 옵션 여러 개 넣을 수 있는데, 순서는 상관없는 듯 하다.