- 설치
	- ```shell
	  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
	  ```
	- 버전확인시 오류가 난다면 패스추가
		- ```shell
		  # zshrc에 homebrew path 추가
		  export "PATH=/opt/homebrew/bin:$PATH" >> ~/.zshrc
		  
		  # zshrc 반영
		  source ~/.zshrc
		  ```
- brew 명령어/사용법
	- 최신버전으로 업데이트
		- ```shell
		  brew update
		  ```
-
-
- 참고
	- [Homebrew 설치 및 사용 방법](https://whalec.io/mac/homebrew-%EC%84%A4%EC%B9%98-%EB%B0%8F-%EC%82%AC%EC%9A%A9-%EB%B0%A9%EB%B2%95/)