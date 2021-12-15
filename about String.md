# Template literals #

템플릿 리터럴은 내장된 표현식을 허용하는 문자열 리터럴이다.
 여러 줄로 이뤄진 문자열과 문자 보간기능을 사용할 수 있다. 
`` 을 이용하여 string 사용을 간소화 할 수 있다.

ex)

```
const sayHi = (aName = "juha") => `hello ${aName} lovely to have u`;

console.log(sayHi());

```
*${표현식을 넣거나 string 에서 function을 실행시킬 수 있고 기본적으로 variable을 넣을 수 있다.}

"${}" 을 이용하여 string 내부에서 function을 실행시켜보자.

```
const add = (a, b) => a + b`;

console.log(`hello ${6,6} lovely to have u`);

```
결과값 = hello 12 lovely to have u

------------------------------------------------------------------
# HTML Fragments #

Template literals 을 이용하여 html을 만드는 것도 가능하다. 
ex)
```
const wrapper = document.querySelector(".wrapper");

const addWelcome = () => {
  const div = `
    <div class="Hello">
      <h1 class="title">Helloo</h1>
    </div>
`;
wrapper.innerHTML = div;
};

setTimeout(addWelcome, 2000);
```
결과값 = 2초 후 Helloo 가 브라우저에 뜬다. 
 
# HTML Fragments 2 #

Template literals 을 이용하여 function을 이용한 html을 만들어보았다.

ex)
```
const wrapper = document.querySelector(".wrapper");

const friends = ["me". "lynn","dal","mark"];

const list = `
  <h1>People i love</h1>
    <ul>
      ${friends.map(friend => `<li>${friend}</li>`).join("")}
    </ul>

`;

wrapper.innerHTML = list;

``` 
*.join : split 처럼 엘리먼트를 나눠주는 역할을 한다. join 같은 경우 문자열로 융합되는 성질을 가지고 있다. 예제에서는 공백을 추가함 으로써 array가 가지고 있는 "," 를 지워주었다. 

-----------------------------------------------------------------------
# More String Improvements # 
