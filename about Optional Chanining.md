# Optional Chanining

예상한 것을 (API 등이) 가지고 있는지 아닌지 확신할 수 없을 때 사용한다.

 ex)
```
console.log(juha?.profile?.email?.provider?.name);
```
//설명: juha가 있는지 확인 있다면 profile이 있는지 확인 있다면 ...반복 후 모두 존재한다면 name 출력. 없다면 출력하지않는다.
