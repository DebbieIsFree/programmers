
1) 문제 자체는 매우 쉽다.
2) 하지만 시간 초과와 효율성 부분에서 합불의 당락이 갈린다.

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
