## 깃허브 공부용 레퍼지토리

### 첫 세팅
````
git config --global user.email "kdh940@gmail.com"
````
깃 글로벌 유저 이메일 설정
----
````
git config --global user.name "DNGHKM"
````
깃 글로벌 유저 이름 설정
----
````
ssh-keygen
````
ssh 키 생성
----
````
cat [pub키 경로]
````
pub 키 내용 확인 -> 깃에 등록해야 IDE 등과 연동 됨


### 깃 사용
폴더 경로 이동 후
````
git init
````
git 초기화(깃으로 관리하겠다) 실시 -> 숨김폴더로 .git 폴더 생성됨
생성된 git 폴더 삭제하면 사용 해제됨
----

.gitignore
사용자가 git에 커밋되지 않길 원하는 파일 또는 폴더들의 목록을 저장, 해당 파일/폴더는 커밋 시 제외됨 

### 깃 저장소 개념
- **Working Directory : 작업하는 파일이 있는 디렉토리**
- **Staging Area : git에 등록할(커밋) 파일들이 올라가는 영역**
- **Local Repository : 로컬 git 프로젝트의 메타데이터와 데이터 정보가 저장되는 영역 (git init 하거나 remote repository를 복사해서 옮겨와서)****
- **Remote Repository  : github 등의 서비스를 통한 온라인 상의 저장소**

(1) git **add** -> (2) git **commit** -> (3) git **push**
반대로는 (4) git **fetch** / (5) git **merge** -> (4) + (5) = **pull**

(1) : Working Directory -> Staging Area
(2) : Staging Area -> Local Repository
--- 여기까진 로컬 ---
(3) : Local Repository -> Remote Repository
--- 여기가 깃허브로 올리는부분 ---

(4) : Remote Repository  -> Local Repository
(5) : Local Repository -> Woking Directory


### 터미널 명령어
````
 git clone [원격저장소 주소]
````
 클론
----
````
git status
````
저장소의 상태를 보여준다
----
````
git add
````
add 수행 (-i : 추가되지 않은 파일 모두 한번에 staging area에 추가)
---- 
````
git rm --cached [파일경로] 
````
staging area에 있는 파일 working directory로 내림
----
````
git rm -r --cached [파일경로] 
````
staging area에 있는 파일  모두 working directory로 내림
----
````
git commit -m "커밋 메시지"
````
커밋
----
````
git push
````
푸시

