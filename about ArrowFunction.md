## arrow functions

arrow function이란 코드를 보기 쉽게 만든 표현 방식. (=>)

ex) 기존 function 방식

```
const names =['tomato', 'potato','banana'];

const dotted = names.map(function(item){
return item + ".";
});

console.log(dotted);
```
*map? 각각의 아이템마다 함수를 호출해준다. return (itme)이 반드시 필요하다.

ex) arrow function 방식 

```
const names =['tomato', 'potato','banana'];

const dotted = names.map(item => item + ".");

console.log(dotted);
```

핵심은 implicit return 을 이용한 점이다. 

*implicit return = "같은 줄"에 어떤 것을 적던지 return 시켜주는 방식. {}은 implicit return을 막기 때문에 오브젝트 리턴시 ()로 감싸주자.

++ 추가 설명

(아이템 값이 두 개인 경우)

```
const names =['tomato', 'potato','banana'];

const dotted = names.map((item,index) => item + "." + index); // index는 숫자를 붙여준다.

console.log(dotted);
```

(아이템 값이 없는 경우)

```
const names =['tomato', 'potato','banana'];

const dotted = names.map(() => "."); // 결과값은 점만 찍힌 리스트 값이 출력

console.log(dotted);
```

