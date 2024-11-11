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
				  saws iam create-group --group-name <group-name>
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
			- 유저 생성
				- ```shell
				  aws iam create-user --user-name <username>
				  ```
			- 사용자를 그룹에 추가
				- ```shell
				  aws iam add-user-to-group --user-name <username> --group-name <group-name>
				  ```
			- 사용자를 그룹에서 제거
				- ```shell
				  aws iam remove-user-from-group --user-name <username> --group-name <group-name>
				  ```
			- 유저에게 정책 연결(그룹은 안됨 개별만)
				- ```shell
				  aws iam attach-user-policy --user-name <username> --policy-arn <policy-arn>
				  ```
			- 유저의 콘솔 로그인용 패스워드 설정
				- ```shell
				  aws iam create-login-profile --user-name <username> --password <password> --password-reset-required
				  ```
			- 엑세스키 생성
				- ```shell
				  aws iam create-access-key --user-name <username>
				  ```
			-
-