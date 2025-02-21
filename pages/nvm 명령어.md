- #resources research
	- **내용**
		- 설치관련
			- ```
			  nvm install <version>       # 특정 버전 설치 (예: nvm install 18.17.0)
			  nvm install node            # 최신 안정(stable) 버전 설치
			  nvm install --lts           # 최신 LTS(Long Term Support) 버전 설치
			  ```
		- 버전 전환 및 사용
			- ```shell
			  nvm use <version>           # 특정 버전 사용 (예: nvm use 18.17.0)
			  nvm use node                # 최신 버전 사용
			  nvm use --lts               # 최신 LTS 버전 사용
			  nvm alias default <version> # 기본 사용 버전 설정
			  ```
		- 버전 확인 및 관리
			- ```shell
			  nvm list                    # 설치된 Node.js 버전 목록 확인
			  nvm ls                      # nvm list의 약어
			  nvm list-remote             # 설치 가능한 모든 원격(Node.js) 버전 확인
			  nvm current                 # 현재 사용 중인 Node.js 버전 확인
			  node -v                     # 현재 Node.js 버전 확인 (nvm 외부 명령어)
			  ```
	- **관련 프로젝트**
	- **영역**
		- [[프로그래밍]]
	- **출처**
	- **태그**
		- #nvm #명령어
	- **메모**
-