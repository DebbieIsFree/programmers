* 출처 : https://www.youtube.com/watch?v=YFIusM9mALg&list=PLlV7zJmoG4XJPcMdCZ0OApBG3VUx4infK

<br>

1) 정렬로 푸는 방법
```
- participant 배열과 completion 배열을 각각 오름차순 (이름순)으로 정렬한다.
- participant 배열을 기준으로 하나씩 증가시키며 completion 배열과 비교한다.
- 인덱스가 i일 때, participatn와 completion 배열값이 다른 배열의 요소(=이름)가 답이 된다.
- (중요!!) 예외처리 : 만약, completion 배열을 끝까지 돌렸어도 답이 안 나올 수 있다.
  (왜냐면 participant 배열이 항상 completion 배열보다 1개 많기 때문이다.)
- 그래서 participant의 마지막 원소가 답이 될 수 있다. 이것에 대한 처리를 해줘야 한다.
```
<br>

2) 해시로 푸는 방법
```
- 순서가 중요하지 않으므로 <unordered_map>을 사용한다.
- 동명이인이 있을 수 있으므로 이름을 key 값으로 하여 value를 증가시킨다.
- 완주하지 못한 사람은 1명이므로, 완주한 배열 (completion)을 돌며 map의 값을 하나씩 감소시킨다.
- 하나를 제외한 모든 map의 원소는 값이 0이므로, 값이 1인 map의 요소를 찾으면 된다.
- 참고) 향상된 for문을 사용하면 코드가 간결해지고 좋다.
```

<br>

3) 그 외
```C++
vector<string> participant;

// auto를 사용한 향상된 for문!!
for(auto player : participant){
  if(map.end() == map.find(player)){
    map.insert(make_pair(player, 1));
  }
  else{
    map[player]++;
  }
}
```
