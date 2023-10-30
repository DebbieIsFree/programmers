


1) c++ vector STL의 search() 함수..!!
2) 이 문제.. 시간 초과가 복병이다..
3) 시간 초과 고려해서 바꿨는데도 시간 초과가 난다..!!! 으아아악
```C++
int solution(vector<int> ing) {
    int answer = 0;

    vector<char> cv;
    for (int i = 0; i < ing.size(); i++) {
        cv.push_back(ing[i] + '0');
    }

    while (1) {
        auto it = search(cv.begin(), cv.end(), "1231", "1231" + 4);

        if (it == cv.end()) {
            break;
        } else {
            cv.erase(it, it + 4);
            answer++;
        }
    }
    return answer;
}
```

