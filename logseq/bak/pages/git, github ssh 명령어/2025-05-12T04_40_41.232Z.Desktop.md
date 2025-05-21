- resource
	- **내용**
		- ssh
		  collapsed:: true
			- ssh 연결확인
				- ```apl
				  ssh -T git@[호스트 별칭]
				  ```
		- git commit
		  collapsed:: true
			- 가장 최근의 커밋 수정
				- ```shell
				  git commit --amend
				  ```
		- git branch
		  collapsed:: true
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
		  collapsed:: true
			- 대상 커밋 이후의 커밋을 취소하고 커밋 내용을 워킹 디렉토리로 이동
				- ```shell
				  # 기본설정
				  git reset --mixed [HEAD~숫자입력 or 해쉬코드]
				  ```
			- 대상 커밋 이후의 커밋을 취소하고 커밋 내용을 스테이징 환경으로 이동
				- ```shell
				  git reset --soft [HEAD~숫자입력 or 해쉬코드]
				  ```
			- 대상 커밋 이후의 커밋을 취소하고 커밋 내용을 완전히 삭제
			  collapsed:: true
				- ```shell
				  git reset --hard [HEAD~숫자입력 or 해쉬코드]
				  ```
		- git revert
			- 대상 커밋 자체를 삭제하지 않고 새로운 커밋 으로 작성
				- ```shell
				  git revert [HEAD~숫자입력 or 해쉬코드]
				  ```
			- 자동으로 커밋을 만들지 않고 내용만 워킹 디렉토리로 이동
				- ```shell
				  git revert -n [HEAD~숫자입력 or 해쉬코드]
				  ```
			- 자동으로 커밋을 메세지 작성
				- ```shell
				  git revert --no-edit [HEAD~숫자입력 or 해쉬코드]
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
	- **출처**
	- **태그**
		- #git #github #명령어
	- **메모**