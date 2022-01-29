### map

map메소드는 주어진 함수를 배열 각 요소에 입력한 후 새로운 배열을 반환한다.


ex)
```
const names= ["juha","mango","hapi"];
const condition = x => x + "♡";
const hearts = names.map(condition);
console.log(hearts);

//result = ["juha♡","mango♡","hapi♡"]
```
-------------------------------------------------------
### filter

filter메소드는 주어진 함수의 테스트를 통과하는 모든 요소를 모아 새로운 배열을 반환한다.

ex)
```
const email = ["cat@naver","dog@naver","wolf@gmail","brid@gmail"];
const noGmail = email.filter(x=> !x.includes("@gmail"));
console.log(noGmail);

//result = ["cat@naver","dog@naver"]
```
-------------------------------------------------------
### find

find메소드는 주어진 판별함수를 만족하는 첫 번째 요소의 값을 반환한다.<br>
그런 요소가 없다면 undefined를 반환한다.


ex)
```
const email = ["cat@naver","dog@naver","wolf@gmail","brid@gmail"];
const foundmail = email.find(x => x.includes("@gmail"));
console.log(foundmail);

//result = wolf@gmail

const list = [1,2,3,4,5,6,7,8,9,10];
const condition = list.find(x => x > 5);
console.log(condition);

//result = 6
```
