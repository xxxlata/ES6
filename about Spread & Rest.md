### spread(...)

변수를 가져와서 풀어헤치고 전개하는것. (unpacked)<br>

ex) 변수 두가지의 요소를 전부 출력해보자.<br>
```
const num = [1,2,3];
const str = ["a","b","c"];

console.log(num , str);
//결과 =[ 1, 2, 3 ] [ 'a', 'b', 'c' ]
console.log([num,str]);
//결과 =[ [ 1, 2, 3 ], [ 'a', 'b', 'c' ] ]

//위 두가지 콘솔출력을 이용하면 두가지의 array 자체가 출력이된다. 이럴 때 spread를 사용하여 출력한다면 배열의 요소를 출력할 수 있다. 

console.log(...num, ...str);
```
object 예제
```
const hapi ={
    h_age: 10,
    h_name: "hapi",
};
  
const mango ={
    m_age: 9,
    m_name:"mango",
};

console.log({ ...hapi , ...mango});
//object를 spread로 전개 하려면 중괄호로 감싸줘야한다.
```
----------------------------------------------------------
### Spread Applications

spread는 추가도 가능하다. 그러나 기존 변수에 push를 하는 것이 아닌 새로운 변수에 복사한 기존 변수들과 더불어 추가가 되는 것이다.<br>
```
const first = ["mon","tue","wed"];
const weekend = ["sat","sun"];
const fullweekend = [...first, "thu", "fri", ...weekend];

console.log(fullweekend);
//결과 = [
  'mon', 'tue',
  'wed', 'thu',
  'fri', 'sat',
  'sun'
]
```
선택적인 속성값(optional object property) 예제
```
const lastName = prompt("Last name");

const user = {
  username: "juha",
  age: 26,
  ...(lastName !== "" && { lastName })
};

console.log(user);

//브라우저에 prompt명령어로 last name을 물었을 때 해당사항을 빈칸으로 두고 넘어갔다면 lastName 키값이 출력되지않게 한다. 
```
--------------------------------------------------
### rest parameters

spread 에서는 요소를 전개했다면, rest는 그 반대로 축소하는 개념이다. 끝도 없는 파라미터값을 받는 함수를 예제로 들어보자.<br>

*rest는 array를 만든다. <br>
```
const infiniteArgs = (...args) => console.log(args);

infiniteArgs("1","juha",2,3,4,5,"haha");
//결과값 =['1', 'juha', 2, 3, 4, 5, 'haha']
//(...args) 가 바로 rest 구문인 것이다. 파라미터에 얼만큼 집어넣어도 ...args 안으로 들어가서 출력된다.
```
특정 속성값을 제외시키는 사용예제
```
const bestFriendMaker = (firstone, ...rest) => {
  console.log(`the firstone is ${firstone} `);
  console.log(rest);
};

bestFriendMaker("juha","hapi","mango","mark");
//결과값 = the firstone is juha 
[ 'hapi', 'mango', 'mark' ]
```
-----------------------------------------
#### spread + rest + destructuring
