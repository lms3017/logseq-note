- IAM
  - 사용자 그룹
    - 사용자 그룹 생성
      - ```shell
        aws iam create-group --group-name <group-name>
        ```
    - 사용자 그룹 삭제
      - ```shell
        aws iam delete-group --group-name <group-name>
        ```
    - 등록된 사용자 그룹 보기
      - ```shell
        aws iam list-groups
        ```
    - 등록된 사용자 그룹에 연결된 정책 목록을 확인
      - ```shell
        aws iam list-attached-group-policies --group-name <group-name>
        ```
    - 그룹에 정책(권한) 연결
      - ```shell
        aws iam attach-group-policy --group-name <group-name> --policy-arn <policy-arn>
        ```
    - 그룹에서 정책(권한) 제거
      - ```shell
        aws iam detach-group-policy --group-name <group-name> --policy-arn <policy-arn>
        ```
    - 사용자를 그룹에 추가
      - ```shell
        aws iam add-user-to-group --user-name <username> --group-name <group-name>
        ```
    - 사용자를 그룹에서 제거
      - ```shell
        aws iam remove-user-from-group --user-name <username> --group-name <group-name>
        ```
  - 사용자
-
