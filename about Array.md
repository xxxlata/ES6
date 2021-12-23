# Array.from() and Array.of() 

### Array.of()
body에 어떤 값을 주던 array로 만들어준다.

기존 array 예제
```
const foods = ["tomato","potato","pizza"];
```

Array.of() 사용예제

```
const foods = Array.of("tomato","potato","pizza");
``` 
-------------------------------------------------------------------------------------

### Array.from()

array-like object로 부터 array를 만드는 메소드이다.
아래 예제와 같이 html을 다룰 때에는 array를 얻지못하고 array-like object를 얻게된다. 그럴 때 array로 바꿔서 사용가능하다.

ex)
html파일에 button을 10개 만들어준다.
```
//button{$}*10 로 button 10개에 각각 1부터 10의 수를 넣어준다. 시간을 단축할 수 있다.
```
Array.from()을 이용한 예제
```
const buttons = document.getElementsByClassName("btn");

Array.from(buttons).forEach(button => {button.addEventListener(
"click",() => console.log("i ve been clicked"))});
```

변수를 이용한 예제
```
const buttons = document.getElementsByClassName("btn");

const ar = Array.from(buttons);

ar.forEach(button => {button.addEventListener(
"click",() => console.log("i ve been clicked"))
});
```
