- #resources
	- **내용**
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
				- pyenv global [특정버전]
			- 현재 프로젝트에서만
				- ```shell
				  pyenv local [특정버전]
				  ```
			- 현재 쉘에서만
				- ```shell
				  pyenv shell [특정버전]
				  ```
	- **출처**
	- **태그**
		- #pyenv #명령어
	- **메모**
		- 메모 작성