
1) 문제 자체는 매우 쉽다.
2) 하지만 시간 초과와 효율성 부분에서 합불의 당락이 갈린다.
3) 처음에는 이중 for문을 사용하려 했으나, 그러면 최악의 경우 10<sup>4</sup> * 10<sup>4</sup>으로 10<sup>8</sup>이 되어 제한시간 1초(보통 10^6)를 초과하게 된다.
4) 그래서 while문과 for문을 혼합하는 방식으로 사용
```C++
int solution(int n) {
    int answer = 1;
    
    int idx = 1;
    
    while(idx < n){
        int sum = 0;
        for(int i=idx; i<n; i++){
            sum += i;
            if(sum == n){
                answer++;
                break;
            }
            if(sum > n){    // for문을 다 돌지 않고도 연속된 숫자의 합이 n보다 커지면 종료해야 한다. (안 그러면 시간초과 에러 뜬다.)
                break;
            }
        }
        idx++;
    }
    
    return answer;
}
```
