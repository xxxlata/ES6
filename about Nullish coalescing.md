# Nullish coalescing 연산자

(??) ||(or)와 같은 논리연산자 이다.

오직 변수값이 null 이거나 undefined 값일 때 작동한다.

||(or)연산자는 boolean 연산자로써 참과 거짓으로만 판단이 가능하다. 숫자 0 이나 문자열의 빈칸을 false 값으로 인식하는데, 이때 Nullish coalescing(??) 연산자를 사용하면 문제를 해결할 수 있다. 

ex)
```

let point = 0;

console.log("hello", point);

//결과값  = hello undefined

console.log("hello", point || "anonymous");

//결과값 = hello anonymous
```
설명: "hello" point 에서 값이 0인 변수는 undefined 가 출력된다. 즉 false 값인 셈이다. 이 때 || 연산자로 넘어가게됨으로써 "anonymous" 가 출력된다. 

?? 연산자를 사용한 ex)
```
let point = 0;

console.log("hello", point);

//결과값  = hello undefined

console.log("hello", point ?? "anonymous");

//결과값 = hello 0
```
설명: || 연산자가 false 값으로 인식하는 0 이나 ("")빈 문자열을 사용하고자 할 때에 ?? 연산자를 이용하여 출력할 수 있게되었다.
