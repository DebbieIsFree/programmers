

1) C++ (문자열 & 비문자열) 연결 : to_string() 사용

``` C++
string answer = "";
answer += "김서방은 ";
answer += to_string(i);
answer += "에 있다";
```
<br>

2) C++ 문자열 비교
 - 방법1) str1.compare(str2) : 0이면 같은 문자열
 - 방법2) str1.find(str2) : str1 문자열 '안'에 str2가 있는지 확인, 0이면 존재
<br>

3) C 문자열 비교
 - <string.h> 헤더 파일
 - strcmp(str1, str2) : 0이면 같은 문자열
