- /
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
	- **출처**
	- **태그**
		- #homebrew #설치
	- **메모**