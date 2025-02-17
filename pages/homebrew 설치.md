- #resources research
	- **내용**
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
	- **관련 프로젝트**
	- **영역**
		- [[프로그래밍]]
	- **출처**
		- [Homebrew 설치 및 사용 방법](https://whalec.io/mac/homebrew-%EC%84%A4%EC%B9%98-%EB%B0%8F-%EC%82%AC%EC%9A%A9-%EB%B0%A9%EB%B2%95/)
	- **태그**
		- #homebrew #설치
	- **메모**
-