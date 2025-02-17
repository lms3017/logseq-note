- #resources research
	- **내용**
		- 설치
			- ```shell
			  brew install nvm
			  ```
		- 환경변수 설정
			- 디렉토리 생성
				- ```shell
				  mkdir ~/.nvm
				  ```
			- .zshrc 설정
				- ```shell
				  export NVM_DIR="$HOME/.nvm"
				  [ -s "/opt/homebrew/opt/nvm/nvm.sh" ] && \. "/opt/homebrew/opt/nvm/nvm.sh"  # This loads nvm
				  [ -s "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm" ] && \. "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm"  # This loads nvm bash_completion
				  ```
			- 적용
				- ```shell
				  source ~/.zshrc
				  ```
		- nvm 명령어/사용법
	- **관련 프로젝트**
	- **영역**
		- [[프로그래밍]]
	- **출처**
		- [NODE-📚-NVM-모듈-사용법-노드-버전-관리](https://inpa.tistory.com/entry/NODE-%F0%9F%93%9A-NVM-%EB%AA%A8%EB%93%88-%EC%82%AC%EC%9A%A9%EB%B2%95-%EB%85%B8%EB%93%9C-%EB%B2%84%EC%A0%84-%EA%B4%80%EB%A6%AC)
	- **태그**
		- #node #nvm #설치
	- **메모**