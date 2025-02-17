- #resources research
	- **내용**
		- 포인터
			- 포인터는 다른 변수의 메모리 주소를 저장하는 변수
			- `type* 변수명` 형태로 선언
			- 주소연산자 `&`
				- 변수의 메모리 주소를 가져온다
			- 역참조 연산자 `*`
				- 포인터가 가리키는 주소에 저장된 값을 참조
			- ```c++
			  int a = 10;
			  int* ptr = &a; 
			  cout << ptr; // a의 주소값을 출력
			  cout << *ptr; // a의 값을 출력
			  cout << &ptr; // ptr의 주소값을 출력
			  ```
		- 참조자
			- `type& 변수명` 형태로 선언
			- ```c++
			  int a = 10;
			  int& ref = a;
			  ref = 20;      // a의 값이 20으로 변경됨
			  cout << a;     // 출력: 20
			  ```
		- 멤버
			- 클래스 내부에 정의된 변수와 함수를 모두 포함하는 용어
			- `const` 맴버함수, 일만 맴버함수
				- | 특성 | `const` 멤버 함수 | 일반 멤버 함수 |
				  | ---- | ---- | ---- |
				  | **객체 상태 변경** | 상태 변경 불가 | 상태 변경 가능 |
				  | **호출 가능 객체** | `const` 객체에서만 호출 가능 | `const` 객체에서는 호출 불가 |
				  | **주요 용도** | 객체 상태를 읽기만 하고, 수정하지 않는 함수 | 객체 상태를 변경하는 함수 |
				  | **예시** | `int getValue() const` | `void setValue(int v)` |
			- static 멤버
				- 모든 클래스 인스턴스에서 공유됨
				- static함수의 경우 non-static데이터는 접근불가
			- protected 멤버
				- 부모에서 상속받은 경우 부모의 protected 멤버 사용가능
		- 생성자
			- 기본 생성자
				- `MyClass(int val)` 형식으로 작성
				- 사용시 ex: `MyClass obj1(10)`
			- 복사 생성자
				- `MyClass(const MyClass& other) {` 형식으로 작성
				- 사용시 ex: `MyClass obj2 = obj1`
			- 이동 생성자
				- `MyClass(MyClass&& other) noexcept {` 형식으로 작성
				- 사용시 ex: `MyClass obj3 = move(obj1)`
		- 연산자
			- 전위 연산자
				- ```c++
				  ClassName& operator++(){
				    	...
				    	return *this; // 증가된 값을 가진 객체 반환
				  }
				  ```
			- 후위 연산자
				- ```c++
				  ClassName& operator++(int) {
				    	ClassName temp = *this;  // 현재 객체를 임시로 저장
				      ...
				    	return temp;  // 증가하기 전 값을 가진 객체 반환
				  }
				  ```
			- 형변환 연산자
				- ```c++
				  operator int() const { // 객체를 int로 변환
				      ...
				  }
				  ```
		- STL 컨테이너
			- 시퀀스 컨테이너 `vector`, `deque`, `list`
			  collapsed:: true
				- ```c++
				  #include <vector>
				  #include <iostream>
				  using namespace std;
				  
				  int main() {
				      vector<int> v = {1, 2, 3};
				      v.push_back(4);  // 끝에 추가
				      v.pop_back();    // 끝에서 제거
				  
				      for (int n : v) {
				          cout << n << " ";  // 출력: 1 2 3
				      }
				      return 0;
				  }
				  ```
			- 연관 컨테이너 `set`, `map`, `multiset`, `multimap`
			  collapsed:: true
				- ```c++
				  #include <map>
				  #include <iostream>
				  using namespace std;
				  
				  int main() {
				      map<string, int> scores;
				      scores["Alice"] = 90;
				      scores["Bob"] = 85;
				  
				      for (const auto& [key, value] : scores) {
				          cout << key << ": " << value << endl;  // 출력: Alice: 90, Bob: 85
				      }
				  
				      return 0;
				  }
				  ```
			- 컨테이너 어댑터 `stack`, `queue`, `priority_queue`
			  collapsed:: true
				- ```c++
				  #include <stack>
				  #include <iostream>
				  using namespace std;
				  
				  int main() {
				      stack<int> s;
				      s.push(1);
				      s.push(2);
				      s.push(3);
				  
				      while (!s.empty()) {
				          cout << s.top() << " ";  // 출력: 3 2 1
				          s.pop();
				      }
				  
				      return 0;
				  }
				  ```
		- 추상 클래스
			- ```c++
			  class AbstractClass {
			  public:
			      virtual void display() = 0; // 순수 가상 함수
			  };
			  ```
		- 구조체
			- 클래스와 유사
			- 주로 여러 변수(데이터 멤버)를 하나로 묶어 표현할 때 사용
			- 기본은 퍼블릭이다.
		- 인라인 함수
			- 함수를 호출하는 대신 그 함수의 코드가 호출된 위치에 직접 삽입
			- ```c++
			  inline int square(int x) {
			      return x * x;
			  }
			  
			  int main() {
			      int a = 5;
			      int result = square(a);  // 컴파일 타임에 square(a)는 a * a 로 교체되서 실행됨
			      cout << "Square of " << a << " is " << result << endl;
			      return 0;
			  }
			  ```
		- 컴파일 타임과 런타임의 차이점
			- | 구분 | 컴파일 타임 (Compile Time) | 런타임 (Runtime) |
			  | ---- | ---- | ---- |
			  | **시점** | 프로그램이 실행되기 전에 | 프로그램이 실행 중일 때 |
			  | **예시** | 변수 선언, 상수 값 할당, 컴파일러 최적화 | 동적 메모리 할당, 사용자 입력 처리 |
			  | **오류 발생** | 구문 오류, 타입 오류 | 실행 도중 오류(예: NULL 포인터, 배열 범위 초과 등) |
			  | **작업** | 코드 분석, 최적화, 함수 인라인화 등 | 실행, 메모리 할당, I/O 처리 등 |
		- 다중정의(오버로딩)
			- 함수 이름은 같지만, 매개변수가 다름
			- 반환 타입만 다르면 오버로딩이 성립안됨
		- 멤버 초기화 리스트
			- ```c++
			  class MyClass {
			  private:
			      int a;
			      int b;
			  
			  public:
			      MyClass(int t) : a(0), b(t) {}  // 초기화 리스트에서 초기화
			  };
			  ```
			- `MyClass(int t) : a(0), b(t) {}` or `MyClass(int t){ a = 0, b = t }` 두방법이 있지만 상수, 참조형 멤버 변수, 상속받은 변수일 경우 멤버 초기화 리스트로만 초기화가 가능하다
			- `b(t)` 이걸 ` b{t}` 이런식으로 표현도 가능하다.(거의 같음)
	-
	- **출처**
	- **태그**
		- #방통대 #c++
	- **메모**
-