- resource
	- **내용**
		- IAM
			- 사용자 그룹
				- 읽기
					- 등록된 사용자 그룹 보기
						- ```shell
						  aws iam list-groups
						  ```
					- 사용자 그룹에 연결된 정책 목록 확인
						- ```shell
						  aws iam list-attached-group-policies --group-name <group-name>
						  ```
					- 사용자 그룹에 연결된 인라인 정책 목록 확인
						- ```shell
						  aws iam list-group-policies --group-name <group-name>
						  ```
				- 쓰기
					- 사용자 그룹 생성
						- ```shell
						  aws iam create-group --group-name <group-name>
						  ```
					- 사용자 그룹 삭제
						- ```shell
						  aws iam delete-group --group-name <group-name>
						  ```
					- 그룹에 정책(권한) 연결
						- ```shell
						  aws iam attach-group-policy --group-name <group-name> --policy-arn <policy-arn>
						  ```
					- 그룹에서 정책(권한) 제거
						- ```shell
						  aws iam detach-group-policy --group-name <group-name> --policy-arn <policy-arn>
						  ```
			- 사용자
				- 읽기
					- 유저정보 확인
						- ```shell
						  aws iam list-users
						  ```
					- 유저가 속한 사용자 그룹 확인
						- ```shell
						  aws iam list-groups-for-user --user-name <username>
						  ```
					- 유저에게 연결된 관리형 정책 확인
						- ```shell
						  aws iam list-attached-user-policies --user-name <username>
						  ```
					- 유저에게 연결된 인라인 정책 확인
						- ```shell
						  aws iam list-user-policies --user-name <username>
						  ```
						- 각 인라인 정책 내용 확인
							- ```shell
							  aws iam get-user-policy --user-name <username> --policy-name <policy-name>
							  ```
					- 유저가 가지고 있는 모든 엑세스키 확인
						- ```shell
						  aws iam list-access-keys --user-name <username>
						  ```
					- MFA 디바이스 확인
						- ```shell
						  aws iam list-mfa-devices --user-name <username>
						  ```
				- 쓰기
					- 유저 생성, 삭제
						- ```shell
						  aws iam create-user --user-name <username>
						  ```
					- 유저를 그룹에 추가, 제거
						- ```shell
						  aws iam add-user-to-group --user-name <username> --group-name <group-name>
						  ```
						- ```shell
						  aws iam remove-user-from-group --user-name <username> --group-name <group-name>
						  ```
					- 유저에게 관리형 정책 연결, 삭제
						- ```shell
						  aws iam attach-user-policy --user-name <username> --policy-arn <policy-arn>
						  ```
						- ```shell
						  aws iam detach-user-policy --user-name <username> --policy-arn <policy-arn>
						  ```
					- 유저에게 인라인 정책 추가(수정), 삭제
						- ```shell
						  aws iam put-user-policy --user-name <username> --policy-name <policy-name> --policy-document <policy-document>
						  ```
						- ```shell
						  aws iam delete-user-policy --user-name <username> --policy-name <policy-name>
						  ```
					- 유저의 콘솔 로그인용 패스워드 설정, 수정
						- ```shell
						  aws iam create-login-profile --user-name <username> --password <password> --password-reset-required
						  ```
							- `--password-reset-required`: 로그인시 패스워드 재설정
						- ```shell
						  aws iam update-login-profile --user-name <username> --password <new-password> --password-reset-required
						  ```
					- 엑세스키 생성
						- ```shell
						  aws iam create-access-key --user-name <username>
						  ```
					-
		- 참고
			- <policy-arn>:: 정책의 arn주소값
			- <policy-document>:: JSON 형식의 정책 문서. `file://`을 접두하로 해서 로컬 파일을 불러온다. ex) `file://s3-read-policy.json`
	- **출처**
	- **태그**
		- #AWS #cli #명령어
	- **메모**
-