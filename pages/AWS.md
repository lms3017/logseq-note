- 루트 계정 생성시 해야할일
	- MFA 설정한다
	- 관리용 사용자를 만들고 AdministratorAccess권한을 부여한다
	  id:: 6734900d-f022-4b14-ad66-39bfcf37b900
	- 관리용 사용자에 자격 증명(Access Key, Secret Access Key)을 추가한다
	- 이후 특별한 경우(결제 정보 변경, 지원 플랜 변경, 계정 폐쇄등)가 아니면 루트 계정을 이용하지 않도록한다
	- 계정 별칭을 지정하고 관리용 사용자로 로그인후 이후작업을 수행한다
	- 관리용 사용자도 MFA 설정한다
	- CloudTrail을 설정한다
	- AWS Config를 활성화하여 AWS 리소스(EC2나 VPC 등)의 구성 변경을 기록한다
		- 설정방법이 어려움 나중에 다시한번 보자
	- Cost Explorer를 활성화하여 요금을 확인할 수 있게 하고, 예산을 설정하고 메일 알림을 설정한다(활성화후 24시간 걸림)
	- Amazon GuardDuty를 활성화하여 보안 위협을 모니터링한다
-
-