# TODAY I LEARN

- 2022.06.20 ~ java와 개발에 필요한 기능을 익히는 중이다.

------

#### 깃(git)

1. 백업
2. 협업
3. 복구

------

1. local repository
   - git init = 새로운 깃 레포지토리를 생성 -> .git
   - git add (파일명) = Staging Area로 올려주는 버전으로 관리할 파일. untracted -> tracked
   - git commit -m 'message' = Staging Area에 올라온 파일을 commit.
   - git log --oneline = commit 히스토리 출력.
   - git diff (commit id) (commit id)
2. remote repository
   - git remote add origin 레포지토리 URL
   - git remote -v = origin으로 지정한 레포지토리 상태를 확인 가능.
   - git push origin master = 로컬과 원격 저장소를 동기화 ( local -> remote )