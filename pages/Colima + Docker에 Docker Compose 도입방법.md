- resource
	- **내용**
		- `brew install docker-compose`로도 설치가 가능하지만 docker-compose명령어만 사용가능함.
		  `docker compose`명령을 사용하기 위해선 수동으로 설치가 필요
		- 설치방법
			- ```shell
			  DOCKER_CONFIG=${DOCKER_CONFIG:-$HOME/.docker}
			  mkdir -p $DOCKER_CONFIG/cli-plugins
			  curl -SL https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-darwin-aarch64 -o $DOCKER_CONFIG/cli-plugins/docker-compose
			  chmod +x $DOCKER_CONFIG/cli-plugins/docker-compose
			  ```
			- 버전이 확인되면 완료
			  ```shell
			  docker compose version
			  ```
	- **출처**
	- **태그**
	- **메모**