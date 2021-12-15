this 와 arrow function

 ex)
```
const button = document.querySelector("button");

button.addEventListener("click", function() {
  this.style.backgroundColor = "red";
});
```
이 예문에서 this는 button을 참조한다. 그러나 arrowfunction을 사용하여 this를 사용한다면 더 이상 button을 참조하지않고 window object를 참조하게 된다. 

따라서 this 키워드를 이용할 때에는 arrowfunction을 이용하지않고 기본 function을 이용하도록 하자.

------------------------------------------------------------------

Arrow Functions in the Real World

array.prototype.find? 제공되는 테스트 조건을 만족하는 첫 번째 엘리먼트 값을 리턴하는 함수이다.

ex)
```
const email = ["nco@no.com","lynn@gmail.com","juha@gmail.com","han@nomad.com"];

const foundMail = email.find(item => item.includes("@gmail.com"));

```

결과값= lynn@gmail.com 을 출력한다.

array.prototype.filter? filter 메소드는 제공된 함수의 조건을 만족한 모든 엘리먼트로 새로운 array를 만들어 낸다. 모든 엘리먼트를 반환함.

ex)
```
const email =[
"nco@no.com",
"lynn@google.com",
"juha@gmail.com",
"juha@nomad.com"
"han@gmail.com"
];

const noGmail = email.filter(item => item.includes("@gmail)");

```
결과값 = ["nco@no.com","lynn@google.com","juha@nomad.com"]

array.prototype.forEach? 각 array의 엘리먼트 마다 제공된 함수를 실행한다.

ex)
```
const email =[
"nco@no.com",
"lynn@google.com",
"juha@gmail.com",
"juha@nomad.com"
"han@gmail.com"
];

email.forEach(email => {
  console.log(email.split("@")[0]);
});

```
*split : 원하는 요소로 엘리먼트를 나눠준다. 이 예제에서 split을 사용하여 "@" 를 기준으로 나누어 주었다.
결과값 = nco lynn juha juha han
