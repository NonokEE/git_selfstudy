## 14) 충돌(conflict)의 개념과 기본 해결 절차

충돌이 생기는 이유 =
두 브랜치가 같은 파일의 같은 줄을 서로 다르게 수정했을 때,
git 입장에선 “시바 뭐 고르라고”라고 할 수 있음.
그럴 때 두 브랜치 개발한 개발자들 둘 다 재판대에 앉혀놓고 누가 뭘 수정해야하는지 판단해줘야 함.

쉽게 얘기하면, merge 했는데 잘 되면 충돌이 아닌거도 안되면 충돌인거임 ㅋㅋ

이건 오류가 아님. 프로젝트 망한거 아님. 정상적인 동작임 (스트레스를 많이 받을 뿐이지.)

---

### git의 동작

1. 삐뽀삐뽀 충돌났습니다. 하고 알리기
    
    ```bash
    git merge feature/conflict-test
    ---
    Auto-merging hello.txt
    CONFLICT (content): Merge conflict in hello.txt
    Automatic merge failed; fix conflicts and then commit the result.
    ```
    
    merge 시점에 이렇게 삐뽀삐뽀 울린다.
    
    ```bash
    git status
    # both modified: hello.txt   ← 충돌난 파일 표시
    ```
    
    status 찍어보면 이렇게 나온다.
    
2. 파일에 충돌 마커 남겨줌
    
    ```bash
    <<<<<<< HEAD
    반가워
    =======
    하이
    >>>>>>> feature/conflict-test
    ```
    
    해당 줄에 대해서 ====가 구분선이고, 위 아래로 각각 어떤 브랜치가 어떤 내용을 담고 있는지 보여줌
    

---

### 해결 절차

1. 충돌난 파일 직접 열어서 수정
    
    ```bash
    <<<<<<< HEAD
    반가워
    =======
    하이
    >>>>>>> feature/conflict-test
    ```
    
    이런 식으로 충돌 마커 남긴다 그랬잖아?
    저거 가짜로 저렇게만 보이는거 아니고, 진짜로 파일에 저렇게 남는거임.
    그래서 “어떻게 하겠다”라고 정하고 저 마커들 다 지워줘야 함
    
    어떻게 할지는 내가 정하는거야
    반가워만 남기든, 하이만 남기든, 둘 다 남기든.
    
    ---
    
    물론 머, 파일 직접 수정하는건 vim같은거 쓸때나 하는 얘기고, vscode에서 하면 accept할지 reject할지 그냥 gui로 눌러서 해결할 수 있음.
    
    ```bash
    Accept Current Change   → HEAD 것 선택
    Accept Incoming Change  → feature 것 선택
    Accept Both Changes     → 둘 다 유지
    Compare Changes         → 나란히 비교
    ```
    
    current/incoming의 관점은 “어디서” merge 커맨드를 쳤는지를 생각하면 알 수 있겠죠?
    
    - UI보기
        
        !image.png
        
        이래 나오는데, text 직접 수정해도 되고, 위에있는거 눌러서 골라도 됨.
        
        GUI에서 클릭하면 되는데 왜 굳이굳이 text 직접 수정을 하느냐?
        
        ```bash
        <<<<<<< HEAD
        main에서 수정한 내용입니다
        =======
        feature-a에서 수정한 내용입니다.
        >>>>>>> feature/conflict-a
        
        ```
        
        이 상황에서
        ”main의 수정내용과 feature-a의 수정내용을 모두 반영했습니다”
        라고 수정할 수도 있는거잖아?
        
        심지어 마커가 남아있더라도 해결 자체는 됨.
        git 입장에서 보면, “그거 그냥 쓰겠다고..? 그래 뭐 알아서 해라..”
        라고 생각하는거라 불가능한건 아님
        대신 코드가 터지겠지.
        
2. 수정 다 됐으면 저장하고 staging
    
    주의해야할게, 이거 지금 “merge”가 안끝난거임. 중간과정에서 멈춘 상태인거야.
    
    그래서 다른거 다른 변경사항이 섞일 수가 없음.
    충돌이 해결되는 시점에 “merge”라는 이벤트가 끝나고 merge commit이 생길거임.
    
    !image.png
    
    vscode ui에서도 staged가 아니라 merge changes라는걸로 바뀜
    옆에 빨간 느낌표도 떠있죠?
    
    !image.png
    
    이렇게 stage 따로 할 수 있습니다.
    
3. 충돌 해결 커밋
    
    merge commit 메시지 자체는 알아서 채워주기때문에, 파일 하나 충돌 해결하면 저장하고 stage만 잘 하면 됨
    여기서 쓰이는 merge commit 메시지는, merge가 conflict 없이 됐을 때 써졌을 내용과 동일함
    파일이 많으면? 다 해결하면 한 번에 커밋 할걸?
    
4. 확인하면됩니다.
    
    

---

### 없던걸로 하지 않을래..?

merge conflict 해결하는 절차 자체가 귀찮다면, 그냥 취소해버릴 수 있음
사용시점은, merge 해놓고 conflict 발생한 상황일 때 (아직 merge 완료 안된거니까 abort 가능)

```bash
git merge --abort
```

일단 취소하고 각자 브랜치에서 적당히 수정한 후 다시 merge할 때 쓰는거.

근데 그렇다고 언제까지고 무를 수는 없는거고, 있던 충돌을 좀 줄이든가 하는거지, 어차피 파일 모양이 달라진거라서 회의를 하든 해서 어캐든 해결은 해야함.

---

### 결론

conflict가 자연스러운 현상이라고는 하지만, 협업하다가 엄청 꼬이면 보통 짜증나는게 아니다.
특히 메인 파이프라인같은거.

그러니까 협업할 때 정책 잘 정해놓고, 인터페이스 설계 잘 해놔야 함
