

1) vector에서 최소값 찾기
```C++
#include <algorithm>

vector<int>v;
...
int num = *min(v.begin(), v.end());    // min까지만 하면 iteraotr 반환됨
```
<br>

2) vector에서 특정 값 위치 찾기
```C++
#include <algorithm>
int num = 3;

// 방법1) iterator
auto it = find(v.begin(), v.end(), num);

// 방법2) 정수값
int n = *find(v.begin(), v.end(), num);
```

<br>

3) vector에서 특정 값의 인덱스 구하기
```C++
#include <algorithm>
int num = 3;

auto it = find(v.begin(), v.end(), num);
it - v.begin();   // 인덱스는 0부터 시작
```

<br>

4) min() VS sort()
```C++
 1) min(tops.begin(), tops.end()); 하면 결과가 뒤죽박죽 이상하게 나오는데
 2) sort(tops.begin(), tops.end()); 정렬한 뒤에, tops[0]로 제일 작은 값을 찾으면 값이 제대로 나오는 기이한 현상..!?!
```

5) 조건 잘 보기..!!
```
len(score) < k 인 케이스와 len(score) >= k 인 케이스로 나누어 처리하는 방식으로 접근했는데
9번, 11번 케이스에서 런타임에러가 발생했습니다.
원인은 9번, 11번이 len(score) < k 인 케이스인 것으로 확인했습니다.

ex) score = [100, 20] 2명인데, 점수가 가장 높은 tops에는 총 3명이 들어갈 수 있다면? --> 1~k번까지, k+1부터 끝까지 하면 에러 발생

-출처: 프로그래머스 답변-
```
   


