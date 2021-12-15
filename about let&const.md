## 1.Dead Zone 

let의 temmporal dead zone? 

ex)let 도입 이전의 코드 

```
var myName = 'juha';
console.log(myName);

결과값 = juha

console.log(myName);
var myName = 'juha';  
결과값 = undefined

```
//자바스크립트의 문법 상 variable 선언은 프로그램 동작 순서에 따라 위에서 시작되는 것 이 맞다.
//그러나 이러한 에러를 잡아내지 못 함. hoisting 하기 때문이다.

*hoisting = 자바스크립트가 프로그램을 작동시키기 전 var값을 위로 옮겨주는 동작.

ex) let 도입 후의 "오작동" 코드

``` 
console.log(myName);
let myName = 'juha';    <- let의 temporal <dead zone> 

결과값 = error
```
## 2.Block Scope

{} 괄호로 이루어진 block scope

```
let hello = hello;  <- 외부의 값
const bye = bye;

function a (){
    console.log(hello);  <- 내부의 값
}
```
let 과 const 는 모두 block scope로 되어있다.
이는 외부에서 (블록)내부로 값을 끌어올 수 있지만 내부에서 외부로 값을 끌어올 수 없다는 것을 의미한다. 
