- #resources
	- **내용**
		- naming 규칙
			- 공통
				- 의미있고 어떤 기능인지 유추 가능한 이름을 사용하도록 한다.
				- index 이외의 중복되는 파일명은 사용하지 않는다.
			- file name
				- 컴포넌트 파일
					- pascal case
					- ex) LoginButton.tsx
				- 커스텀 훅
					- snake case, use + 파일명
					- ex) use_query_param.ts
				- 기타
					- snake case
					- ex) user_helper.ts
			- directory name
				- snake case
				- ex) main_themes
			- function name
				- 컴포넌트
					- pascal case
					- ```typescript
					  function LoginButton() {...}
					  ```
				- 커스텀 훅
					- camel case, use + 함수명
					- ```typescript
					  function useQueryParam() {...}
					  ```
				- 화면조작
					- change, select 이벤트등
					- camel case, handle + 함수명
					- ```typescript
					  function handleOpen() {...}
					  ```
				- 페이지 이동
					- camel case, navigateTo +함수명
					- ```typescript
					  function navigateToHome() {...}
					  ```
				- 기타
					- camel case
					- ```typescript
					  function formatTime() {...}
					  ```
			- type
				- domain
					- pascal case
					- ```typescript
					  type User = {
					    ...
					  }
					  ```
				- state
					- 상태명 + State
					- ```typescript
					  type UserState = {
					    ...
					  }
					  ```
				- props
					- 컴포넌트명 + Props
					- ```typescript
					  type UserProfileProps = {
					    ...
					  }
					  ```
				- 기타
					- pascal case
					- ```typescript
					  type Response = {
					    ...
					  }
					  ```
			- constant
				- upper snake case
				- ```typescript
				  const API_BASE_URL = "..."
				  ```
		- 컴포넌트 작성 규칙
			- 디랙토리 아래의 index파일을 참조 할 수 있도록 한다.
				- ```
				  # 디랙토리
				  src/
				    components/
				      componet/
				        index.tsx
				              
				  # 참조예
				  import Componet from ""@src/components/componet"
				  ```
			- tsx함수는 function을 사용하고 바로 export해준다.
				- ```tsx
				  export default function Componet() {
				    return <div>Componet</div>;
				  }
				  ```
			- 컴포넌트의 내부함수는 arrow function을 사용한다.
				- ```tsx
				  export default function Componet() {
				    const func = () => {
				      ...
				    }
				    return <div>Componet</div>;
				  }
				  ```
			- 컴포넌트의 내부함수및 변수는 아래의 순서대로 작성한다.
				- ```tsx
				  export default function Componet() {
				    ① dispatch, selector
				    
				    ② useState, useRef
				    
				    ③ useEffect
				    
				    ④ 핸들러 및 기타 로직
				    
				    return <div>Componet</div>;
				  }
				  ```
			- 실제로 성능문제가 발생하지 않는 경우는 useMemo, useCallback는 사용하지 않는다.
			- 임포트
				- React관련 함수는 추가 임포트로 사용한다.
					- ```tsx
					  import React, { useEffect, useState } from 'react';
					  ```
				- 아래 예시의 임포트 순서대로 임포트 한다.
					- ```tsx
					  import React, { useEffect, useState } from 'react';
					  ① mui, components, pages
					  
					  ② redux, features, hooks
					  
					  ③ utils, constants, その他
					  ```
	- **출처**
		- 출처 작성
	- **태그**
		- #naming규칙 #코딩컨벤션 #파일명규칙 
		  #디렉토리구조 #함수명규칙 #타입정의 
		  #상수명 #컴포넌트작성 #React #TypeScript
	- **메모**
		- 메모 작성
-