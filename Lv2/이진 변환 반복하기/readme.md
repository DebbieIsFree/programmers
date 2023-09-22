1) 다른 사람 풀이
```C++
// 출처 : 프로그래머스 
#include <string>
#include <vector>
#include <algorithm>
using namespace std;

vector<int> solution(string s) {
    int zeros{0}, num_transform{0}; vector<bool> bin;
    for_each(s.cbegin(),s.cend(),[&bin](const char c){bin.emplace_back(c=='1');});  //s를 이진수로 변환
    while(true){
        if(bin==vector<bool>{true}) break;
        int ones = count(bin.cbegin(),bin.cend(),true);    //1갯수를 셈
        zeros += bin.size()-ones;                          //0갯수를 셈
        bin.clear();
        while(ones>0){ bin.emplace_back(ones%2); ones/=2; }//1갯수를 2진수로 바꿈. 순서는 거꾸로지만 계산에는 영향없음
        ++num_transform;                                   //이진변환 횟수 기록
    }
    return {num_transform,zeros};
}
```
<br>

  1-1) emplace_back()
  - 객체 생성에 필요한 인자만 받은 후 함수 내에서 객체를 생성해 삽입하는 방식
  - 임시 객체를 만들 필요가 없다
```C++
// push_back() 사용 시
vector<item> vt;
item a = {}; // 기본 생성자 호출

vt.push_back(item("abc", 1, 234)); 
vt.push_back(std::move(a)); 

vector<int> v;
v.push_back(1);

// emplace_back() 사용 시
vector<item> vt 

vt.emplace_back("abc",1,234);

// 출처 : https://openmynotepad.tistory.com/10
```
<br>


2) string 관련 참고하기 좋은 자료  <br>
https://blockdmask.tistory.com/338




