# HEAD 개념 실습 기록

## cat .git/HEAD 결과
`ref: refs/heads/main`

## git rev-parse HEAD 결과
`c64d2ad37ebf13043bf64730696445834cdd620e`

## git log --oneline -5 결과
`c64d2ad (HEAD -> main, origin/main, origin/HEAD) docs: update progress - 커밋 기록 조회 심화 완료` </br>
`b00565c practice: add git log advanced practice log` </br>
`907f6ab docs: add project description` </br>
`a739900 fix: add bug fix log` </br>
`c9473a0 feat: add automation script draft` </br>

## HEAD~1 과 HEAD~2 SHA
- HEAD~1: `b00565c2121086ec950b6bf512a71df57f23197d`
- HEAD~2: `907f6abdda03f7ec30551d072383c7eecd7e821b`

## git log --oneline과 대조한 결과
- HEAD~1이 가리키는 커밋 메시지: `practice: add git log advanced practice log`
- HEAD~2이 가리키는 커밋 메시지: `docs: add project description`

## 새로 알게 된 점 또는 특이사항
- HEAD라는거 직관만 있었지 진짜로 뭔지 몰랐었음. </br> 
브랜치를 한번 타고 가서 가리키는거구나. </br> 
커밋이 어떤 브랜치에 속하는지 다루게 하기 위해서 이렇게 구조를 짠건가 싶음. </br> 
- 그럼 나 vscode로 프로젝트 할 때 checkout to로 했었는데 그러면 안되는건가? </br>
-> 아마 vscode에서 알아서 브랜치 가리키게끔 해놨겠지. 어차피 GUI 기반이잖아. </br>
-> 지금보니까 애초에 브랜치를 선택하게 하네. 특정 커밋이 아니라. </br>
-> 특정 커밋을 HEAD로 가리키게 할 일이 있을까 싶긴 함. 근데 그게 된다는건, 할 일이 있다는거임. 나중에 배우겠지.