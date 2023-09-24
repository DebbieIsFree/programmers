
1) Greedy 문제
2) 


```C++
reserve.erase(remove(reserve.begin(), reserve.end(), n), reserve.end());
```
- reserve 컨테이너에서 특정 값을 삭제하는 작업을 수행 
- remove 알고리즘을 사용하여 reserve 컨테이너에서 'n'이라는 값을 찾아서 이 값을 컨테이너에서 제거하고,
- 그 다음에 erase 함수를 사용하여 실제로 삭제. 이렇게 함으로써 'n' 값을 'reserve' 컨테이너에서 제거함.
- remove는 특정 값을 찾아서 완전히 지우는 것이 아닌, 벡터의 뒤로 보내기 때문에 추가로 erase를 해줘야 한다.
