- #resources
	- **내용**
		- 설치
			- ```shell
			  brew install pyenv
			  ```
			- tcl-tk 설치
				- ```shell
				  brew install tcl-tk
				  ```
			- 환경변수 설정
				- .zshrc 설정
					- ```shell
					  # pyenv setting
					  export PYENV_ROOT="$HOME/.pyenv"
					  export PATH="$PYENV_ROOT/shims:$PATH"
					  eval "$(pyenv init --path)"
					  eval "$(pyenv init -)"
					  export LDFLAGS="-L/opt/homebrew/opt/zlib/lib"
					  export CPPFLAGS="-I/opt/homebrew/opt/zlib/include"
					  export PKG_CONFIG_PATH="/opt/homebrew/opt/zlib/lib/pkgconfig"
					  ```
				- 적용
					- ```shell
					  source ~/.zshrc
					  ```
		- pyenv 명령어/사용법
	- **관련 프로젝트**
	- **영역**
		- [[프로그래밍]]
	- **출처**
		- https://deku.posstree.com/ko/environment/pyenv/
	- **태그**
		- #pyenv #설치 #설정
	- **메모**