

1) accumulate
```C++
#include <numeric>

vector<int> v = { 1, 2, 3, 4, 5 };
accumulate(v.begin(), v.end(), 0);    // first iterator, second iterator, initial value of sum (합의 초기값)
```
