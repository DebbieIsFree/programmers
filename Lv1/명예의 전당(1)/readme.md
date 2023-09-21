

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
 2) sort(tops.begin(), tops.end()); 정렬한 뒤에, v[0]로 제일 작은 값을 찾으면 값이 제대로 나오는 기이한 현상..!?!
```
