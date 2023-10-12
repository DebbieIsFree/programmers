
```
< 문제 >
배열 arr에서 연속적으로 나타나는 숫자는 하나만 남기고 전부 제거하려고 합니다.
단, 제거된 후 남은 수들을 반환할 때는 배열 arr의 원소들의 순서를 유지해야 합니다.
```


```C++
<< unique 함수 사용 >>

#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;

vector<int> solution(vector<int> arr) 
{

    arr.erase(unique(arr.begin(), arr.end()),arr.end());

    vector<int> answer = arr;
    return answer;
}
```
<br>

```C++
<< resize 함수 >>
vector.resize(개수, 값)
```
