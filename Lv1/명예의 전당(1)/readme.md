

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

<br>

5) 조건 잘 보기..!!
```
len(score) < k 인 케이스와 len(score) >= k 인 케이스로 나누어 처리하는 방식으로 접근했는데
9번, 11번 케이스에서 런타임에러가 발생했습니다.
원인은 9번, 11번이 len(score) < k 인 케이스인 것으로 확인했습니다.

ex) score = [100, 20] 2명인데, 점수가 가장 높은 tops에는 총 3명이 들어갈 수 있다면? --> 1~k번까지, k+1부터 끝까지 하면 에러 발생

-출처: 프로그래머스 답변-
```

<br>

6) 다른 사람 풀이
```C++
vector<int> solution(int k, vector<int> score) {
    vector<int> answer, tmp;

    for(auto s : score){
        tmp.push_back(s);
        sort(tmp.begin(), tmp.end(), greater<int>());
        if(tmp.size() >= k) tmp.erase(tmp.begin() + k, tmp.end()); // k번째부터 끝까지 삭제
        answer.push_back(tmp.back());
    }

    return answer;

}
```

 6-1) 벡터 특정 원소 지우기 
```C++
// 방법 1
erase(시작, 끝) // [시작, 끝)

// 방법 2 - 벡터 v의 i번째 인덱스에 있는 원소를 삭제하고 싶을 때
erase(v.begin() + i);
```

 6-2) remove()
```C++
#include <algorithm>  // 헤더 파일 포함

remove(first, last, 삭제하려는 값); // 범위는 [first,last)
```

<br>

6-2) 벡터 back() : 벡터의 마지막 요소 반환
<br>

7) vector 메서드
```
size() - 벡터의 요소의 개수를 반환한다.
swap(vector객체) - 두 벡터의 내용을 교환(교체)한다.
empty() - 벡터가 비었는지 여부를 반환한다.
at(index) - index번째 요소에 접근한다.
front() - 벡터의 첫 번째 요소를 반환한다.
back() - 벡터의 마지막 요소를 반환한다.
begin() - 벡터의 첫 번째 요소를 가리킨다.
end() - 벡터의 마지막 요소를 가리킨다.
```

<br>

8) 참고 자료<br>
https://velog.io/@cse_pebb/C-remove-%ED%95%A8%EC%88%98-vs.-vector%EC%9D%98-erase-%ED%95%A8%EC%88%98



