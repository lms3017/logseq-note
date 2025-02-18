- 로그인 관련 정리
	- app.ts
	- auth_route.ts
		- app.group?
	- login_route.ts
		- loginModel,commonModel 미들웨어 역할
	- auth_service.ts
		- 디비데이터 취득등 서비스 관련
	- staff_repository.ts
		- kysely orm 로직
-
- 디렉토리 정리
	- route
		- 라우팅 관련
	- model
		- 유효성 검사등 미들웨어 처리
	- service
		- 서비스관련
	- repository
		- orm 처리관련
-
- 엔드포인트
	- start/work
		- 근무예정 취득
			- ```sql
			  SELECT
			    daily_attendances.*,
			    work_records.started_at,
			    work_records.ended_at
			  FROM
			    daily_attendances
			  LEFT JOIN
			    work_records
			  ON
			    work_records.daily_id = daily_attendances.id
			  WHERE
			    daily_attendances.date = {date_value} AND
			    daily_attendances.staff_id = {staffId_value} AND
			    daily_attendances.tenant_id = {tenantId_value}
			  LIMIT 1;
			  ```
		- 근무예정 있을 경우
			-
		- 근무예정 없을 경우
			- 출근일 취득
				- ```sql
				  SELECT *
				  FROM schedule_patterns
				  WHERE tenant_id = {tenantId_value}
				  AND pattern_code = {patternCode_value}
				  LIMIT 1;
				  ```
			- daily_attendances, work_records에 데이터 추가
				- ```sql
				  INSERT INTO daily_attendances (...)
				  INSERT INTO work_records (...)
				  ```
-
- 질문사항
	- await, then 혼용에서 쓰고 있는데 이유가 있나?
	- api설계서 작성 필요한가?
	-