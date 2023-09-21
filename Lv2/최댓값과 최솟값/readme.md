1) 
```C++
string s = "-1 -2 -3 -4";

for(int i=0; i<s.length(); i++){
  cout << s[i] << " ";    
}

// 결과
- 1 - 2 - 3 - 4   // -1 -2 -3 -4와 같이 출력되지 않는다!!
```

<br>

2) stringstream
```C++
#include <sstream>

string s = "a b c d";

// stringstream 사용법
stringstream stream;
stream.str(s);  // 공백을 기준으로 문자열 파싱
string tmp = "";
while(stream >> tmp){
}
```
