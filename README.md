! 코테 알고리즘 마지막 점검용 !

[ c++ 문법 ]
1. sort
(오름차순)
int a[10] = {9, 3, 5, 4, 1, 10, 8, 6, 7, 2};
sort(a, a+10);

(내림차순)
bool compare(int a, int b){
  return a > b ;
}
sort(a, a+10, compare);

(구조체를 정렬)

struct Point{
  int x;
  int y;
};

bool compare(const Point &p1, const Point &p2){
  if(p1.x < p2.x){
    return true;
  }else if(p1.x == p2.x){
    return p1.y < p2.y;
  }else{
    return false;
   }  
}

sort(a, a+10 , compare);


2. 스택
#include <iostream>
#include <stack>

using namespace std;

int main(){

	// 스택 생성
	stack<int> s;


	// push
	s.push(3);
	s.push(2);
	s.push(1);


	// top
	cout << "top element: " << s.top() << '\n';
	// pop
	s.pop(); // 1이 삭제
	s.pop(); // 2가 삭제


	// size
	cout << "stack size: " << s.size() << '\n';


	// empty
	cout << "Is it empty?: " << (s.empty() ? "Yes" : "No") << '\n';

	return 0;

}
  
  
3. 큐

#include <queue>

queue<int> q;

queue.push(element);
queue.pop();
queue.front();
queue.back();
queue.size();
queue.empty();


==================================================

[ 구현 ]

[ 그리디 ]
그리디를 풀 때에는 이렇게 " 탐욕적으로 풀어도 될련지 ? " 를 꼭 생각해보자 . 

[ dp ]

<< 그리디와 dp를 구분하는 마음가짐 >>
