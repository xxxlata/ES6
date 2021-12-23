# Default Values


Default Values 값에
array 나 object, string, 변수값이 들어갈 수 도 있다.

arrowFunction을 이용한 예제 
```
const sayHi = (aName = "juha") => "hello" + aName;

console.log(sayHi());

//결과값 = hello juha

```

기본 function을 이용한 예제

```
function sayHi(aName) {
return "hello" + aName;
}

console.log(sayHi("juha"));
```
