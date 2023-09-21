

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
