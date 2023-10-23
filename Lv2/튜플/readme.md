

< 좋은 풀이 참고 > <br><br>

1) 숫자가 나온 횟수를 센다. -> 빈도가 높은 숫자부터 answer 벡터에 추가한다.<br>
2) ex) s = "{{2},{2,1},{2,1,3},{2,1,3,4}}" 일 때, 튜플은 [2, 1, 3, 4]이다.<br>
3) 2는 4번, 1은 3번, 3은 2번, 4는 1번 나온다.<br>
4) 따라서 {횟수, 숫자} 벡터에 이를 기록하고, '횟수'를 기준으로 내림차순 정렬하면 답을 구할 수 있다.<br><br>

```C++
#include <bits/stdc++.h>
using namespace std;

vector<int> solution(string s) {
    int st[101010]={};
    vector<int> answer;
    string tmp;
    for(char i: s){
        if(i-'0' >=0 && i-'0' <=9){
            tmp += i;
        }
        else{
            if(tmp.length())
                st[stoi(tmp)]++, tmp.clear();
        }
    }
    vector<pair<int, int>> v;
    for(int i =0; i <101010; i++)
        if(st[i])
            v.push_back({st[i], i});
    sort(v.begin(), v.end());
    reverse(v.begin(),v.end());
    for(auto it: v) answer.push_back(it.second);
    return answer;
}
```

