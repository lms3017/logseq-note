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
	- pyenv 버전확인
		- ```shell
		  pyenv versions
		  ```
	- 설치 가능한 Python 버전을 확인
		- ```shell
		  pyenv install --list
		  ```
	- Python 버전 설치
		- ```shell
		  pyenv install
		  or
		  pyenv install [특정버전]
		  ```
	- 특정 버전으로 전환하기
		- 전역
			- ```shell
			  pyenv global [특정버전]
			  ```
		- 현재 프로젝트에서만
			- ```shell
			  pyenv local [특정버전]
			  ```
		- 현재 쉘에서만
			- ```shell
			  pyenv shell [특정버전]
			  ```
-
- 참고
	- https://deku.posstree.com/ko/environment/pyenv/