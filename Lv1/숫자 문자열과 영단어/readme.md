
1) 엄청난 if-else문 대신 regex_replace()를 사용해서 풀 수 있다.

```C++
#include <regex>
regex_replace(문자열, regex(정규식), 치환할문자열)

s = regex_replace(s, regex("zero"), "0");
s = regex_replace(s, regex("one"), "1");
s = regex_replace(s, regex("two"), "2");

string s = "hello my name is gildong";
s = regex_replace(s, regex("gildong"), "hong");
// 결과 : hello my name is hong
```
<br>


2) 문자열에서 replace 사용법
```C++
문자열.replace(시작위치,길이, 치환할문자열)
```
<br>

3) 참고 자료 <br>
https://jie0025.tistory.com/191
