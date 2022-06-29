# TODAY I LEARN

- 2022.06.20 ~ java와 개발에 필요한 기능을 익히는 중이다.

------

#### 1일차 깃(git)

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


   ---


   # 2일차 (협업)

### 1. Shared Repository Model

- Owner & Collaborator
  - 모든 팀원이 모든 권한을 갖는다.(Push 권한을 갖는다.)
  - 가장 1차원적인 기본이되는 협업의 모델이다.
  - 협업을 할때, 해당 모델만 가지고는 힘들다.

### 2. Fork & Pull Request

* 권한을 가지고 있느냐 없느냐가 가장 큰 차이다.

  * push의 권한이 없기 때문에, pull Request 기여할 수 있다.

  * branch 생성해도 되고 안해도 된다.

    * 근데, 실무에선 pr이 하루에도 수십개가 날아와 하는걸 권장.

     

### 3. 협업과 관련된 git 명령어

1. git remote add origin {repo_url} 
2. git clone {git_repo}  ---> download
3. git push origin master ---> upload
4. git pull origin master ---> update



#### Branch

---

**Pointer**

> branch는 특정 Commit을 바라보는(가리키는) Pointer의 역할을 한다.

- branch 관련 명령어
  - git branch = 브랜치 리스트 보기
  - git branch {브랜치 이름} = 브랜치 생성
  - git switch{브랜치 이름} = 브랜치간의 이동을 할 수 있고 (HEAD가 바라보는 브랜치의 변경이다.)
  - git switch -c {브랜치 이름} = 브랜치 생성과 동시에 해당 브랜치로 이동.
  - git merge{브랜치 이름} = 누가 누구를 머징하는지, (대부분의 경우 master -> 기본 틀이되는 브랜치로 이동하고 merge한다.)
  - git branch -d{브랜치 이름} = -D _merge 되기 전의 브랜치도 삭제될 수 있기 때문에 사용을 주의해야한다. ( d 꼭 소문자로)