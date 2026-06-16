# 로컬 저장소와 원격 저장소의 차이

## 로컬 저장소
- 위치: 작업중인 PC
- 특징: 인터넷이 없어도 작업 가능(말 그대로 로컬이니까)
- 언제 쓰나: 실제 작업용

## 원격 저장소
- 위치: 서비스 주체의 서버 GitHub, BitBucket 등 (즉, 일종의 Cloud Service이기도 함)
- 특징: 각각의 local이 접근가능
- 언제 쓰나: 협업, 백업용

## git remote -v 실행 결과
origin  https://github.com/NonokEE/git_selfstudy.git (fetch)
origin  https://github.com/NonokEE/git_selfstudy.git (push)

## 오늘 새로 알게 된 점
- `git remote -v`로 세부 내용 보는거구나