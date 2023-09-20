
1) 숫자인지 확인하고 싶을 때  --> isdigit() 함수 사용 

```C++
for (int i = 0; i < s.size(); i++)
{
    if (!isdigit(s[i]))
      answer = false;
}
```
