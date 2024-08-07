<<<<<<< HEAD
### ssh 설정
=======
- git 설치
	- mac에서는 기본으로 git이 설치되어 있음.
- ssh 설정
  collapsed:: true
>>>>>>> 1242b34 (Auto saved by Logseq)
	- ```shell
	  cd ~/.ssh ## 없으면 디렉토리 생성 후 이동
	  ssh-keygen -t rsa -C [메일주소] -f [ssh 파일이름] ## 이후 비번입력 따로 안할꺼면 엔터 두번
	  eval "$(ssh-agent -s)" ## 기존 에이전트정보 확인하거나 새로운 ssh-agent 실행
	  ssh-add ~/.ssh/[ssh 파일이름] ## ssh-agent에 ssh-key 추가
	  ssh-add -l ## 추가 됬는지 확인
	  pbcopy < ~/.ssh/[ssh 파일이름].pub ## 공개키 복사
	  vi ~/.ssh/config ## 컨피그파일 생성 / 실행
	  
	  ## config에 해당 내용추가
	  Host [호스트 별칭]
	     HostName github.com
	     User [사용자 이름]
	     IdentityFile ~/.ssh/[ssh 파일이름]
	  		
	  github 로 가서 settings 클릭
	  ssh and gpg keys 클릭
	  new ssh key 클릭 -> title 엔 식별가능하게 쓰고 key에는 복사한 내용을 붙여넣는다
	  
	  ssh -T git@[호스트 별칭] ## 연결확인 테스트. 처음 연결 확인하면 yes를 눌러주면됨 known_hosts, known_hosts.old 가 생긴다
	  
	  ## clone할때 아래의 형식대로 입력하도록 주의
	  git clone git@[호스트 별칭]:[레파지토리경로]
	  
	  git config user.email [메일명] ## 전역에 설정된 값이 들어가서 설정해 줘야됨
	  git config user.name [이름]
	  ```
<<<<<<< HEAD
- ### 명령어 정리
	- ssh
		- ssh 연결확인
			- ```apl
			  ssh -T git@[호스트 별칭]
			  ```
=======
- git 명령어 정리
>>>>>>> 1242b34 (Auto saved by Logseq)
	- git commit
		- 가장 최근의 커밋 수정
			- ```shell
			  git commit --amend
			  ```
	- git branch
		- 로컬 브렌치 원격 레파지토리 연결 확인
			- ```shell
			  git branch -vv
			  ```
		- 현재 위치한 브렌치명 변경
			- ```shell
			  git branch -m [새로운 브렌치명]
			  ```
		- 현재 위치가 아닌 브렌치명 변경
			- ```shell
			  git branch -m [대상 브랜치명] [새로운 브렌치명]
			  ```
		- 브랜치 삭제
			- ```shell
			  git branch -d [대상 브랜치명]
			  ```
	- git reset
		- 해당 커밋을 취소하고 커밋 내용을 스테이징 환경으로 이동
			- ```shell
			  git reset --sorft [HEAD~숫자입력 or 해쉬코드]
			  ```
	- git remote
		- 현재 원격 저장소 확인
			- ```shell
			  git remote -v
			  ```
		- 원격 저장소 URL 변경
			- ```shell
			  git remote set-url origin git@[호스트 별칭]:[레파지토리경로]
			  ```
-