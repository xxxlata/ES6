# for of loof

Array, Iterable,NodeList, Strings 등에 사용 가능하다.

기존 for loof 예시
```
for (let i = 0; i < 20; i++) {
console.log("I love me");
}
```

결과값 = I love me 20번 출력

for ..of 사용 예시

```
const foods = ["pizza","hamburgur", "ice cream"];

for (const food of foods) {
consol.log(food);
}
```

결과값 = 리스트 안의 엘리먼트를 출력한다. foreach 키워드와 비슷하나 foreach는 반드시 리스트여야 가능하고 루프를 사용할 수 없다. 

for of loof 사용예시

```
const foods = ["pizza","hamburgur", "ice cream" , "potato","pop corn"];

for (const food of foods) {
  if(food === "ice cream") {
    break;
} else {
    consol.log(food); 
  }
}
```
결과값 = ice cream에서 출력을 멈춘다.
