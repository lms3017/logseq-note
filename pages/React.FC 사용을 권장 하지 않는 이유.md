- resource
	- **내용**
		- children이 자동으로 포함되서 예상치 못한 동작이 가능
			- ```javascript
			  const FormItem: React.FC = (props) => {
			    console.log(props.children); // 항상 존재함 (undefined가 아님)
			    return <div>{props.children}</div>;
			  };
			  ```
		- 제네릭 사용이 불편함
			- React.FC를 사용한 버전
				- ```javascript
				  const FormItem = <T,>(): React.FC<{ data: T }> => {
				    return ({ data }) => <div>{String(data)}</div>;
				  };
				  ```
			- 아닌 버전
			  id:: 67da7cad-fee1-4cc5-848d-ad45b773d86e
				- ```javascript
				  const FormItem = <T,>({ data }: { data: T }) => {
				    return <div>{String(data)}</div>;
				  };
				  ```
		- MUI, Next.js, Vercel 등의 공식 문서에서도 `React.FC` 사용을 지양
	- **출처**
	- **태그**
		- #React
	- **메모**