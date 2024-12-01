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
- STL 컨테이너
	- 시퀀스 컨테이너 `vector`, `deque`, `list`
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
-