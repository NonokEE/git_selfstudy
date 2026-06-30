# git rm / git mv 실습 기록

## git rm
- 실행한 명령어: `git rm .\git-rm-mv-practice\delete-me.txt`
- git status에서 확인한 내용:
```Powershell
D  git-rm-mv-practice/delete-me.txt
```

## git rm --cached
- 실행한 명령어: `git rm --cached .\git-rm-mv-practice\track-remove.txt`
- 실제 파일이 남아 있었나요? (Y/N): Y
- git status에서 확인한 내용:
```Powershell
D  git-rm-mv-practice/track-remove.txt
?? git-rm-mv-practice/track-remove.txt
```
- 특이사항 : unstaged도 같이 찍힌다
    - 추측컨대, git 추적을 뺐으니 일단 초록 D는 찍힘. 동시에, 더이상 추적이 없으니, git 입장에서는 새로운 untracked 파일이 생겼다고 볼 수 있음.</br>

        실제로 untracked 상태의 파일을 stage하면, 둘이 상쇄되어 변동사항이 없어져버림.

## git mv
- 실행한 명령어: `git mv .\git-rm-mv-practice\old-name.txt .\git-rm-mv-practice\new-name.txt`
- git status에서 확인한 내용:
```Powershell
R  git-rm-mv-practice/old-name.txt -> git-rm-mv-practice/new-name.txt
```
vscode에서는 그냥 `R`만 보이지만, pwsh에서 확인하면 파일 이름이 뭐에서 뭐로 바뀌었는지도 이쁘게 보여준다.