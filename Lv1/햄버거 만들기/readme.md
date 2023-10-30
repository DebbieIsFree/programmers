


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

4) 다른 사람 풀이
5) for문이 10<sup>6</sup>이므로 시간 초과 발생 안 함!
```C++
int solution(vector<int> ing) {
    int answer = 0;
   
    string str = "";
    for(int i=0; i<ing.size(); i++){
        str += to_string(ing[i]);
        if(str.length() >= 4){
            if (str.substr(str.length()-4) == "1231"){
                str = str.substr(0, str.length()-4);
                answer++;
            }
        }
    }
    return answer;
}
```

