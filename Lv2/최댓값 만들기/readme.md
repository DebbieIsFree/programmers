
방법 1) 벡터 오름차순 정렬 
```C++
vector<int> v;
sort(v.begin(), v.end(), greater<int>());
```
<br>

방법 2) 벡터 역방향 반복자 사용
```C++
vector<int>v;
sort(v.rbegin(), v.rend());  // 내림차순 정렬
// v.rbegin() == v.end(), v.rend() == v.begin()
```
