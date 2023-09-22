
1) bitset을 이용한 풀이
```C++
// 출처 : 프로그래머스

#include <bitset>
using namespace std;

int solution(int n) {
    int num = bitset<20>(n).count();

    while (bitset<20>(++n).count() != num);
    return n;
}
```
<br>

2) bitset 사용법
```C++
// bitset 생성 
bitset<6> bit;			// 000000
bitset<6> bit("110011");	// 문자열 "110011"로 초기화
bitset<20> bit2(58);		// 10진수 58로 초기화

int num = 62;
bitset<20> bit2(num);
string s = bit2.to_string();
```


<br>

3) C++ 레퍼런스 및 출처
- https://en.cppreference.com/w/cpp/utility/bitset/count
- https://notepad96.tistory.com/35
