# Array.find() Array.findIndex() Array.fill() 

### Array.find()
부합하는 값을 가진 첫번째 element를 출력한다. 

ex)
```
const friends = [
  "tomato@korea.com",
  "pizza@gmail.com",
  "potato@korea.com",
  "juha@gmail.com"
];

const target = friends.find(friend => friend.includes("@korea.com"));

console.log(target);
```
결과값 =``` tomato@korea.com```

----------------------------------------------------------
### Array.findindex()

element가 어디있는지 알고 싶을때 사용한다.

ex)
```
const friends = [
  "tomato@korea.com",
  "pizza@gmail.com",
  "potato@gorea.com",
  "juha@gmail.com"
];

const check = () => friends.findIndex(friend => friend.includes("@gorea.com"));

let target = check();

if (target !== -1) {
  console.log(target);

  const username = friends[target].split("@")[0];

  const email = "korea.com";

  friends[target] = `${username}@${email}`;

  target = check();
}

console.log(friends);

//결과값 =[
  "tomato@korea.com",
  "pizza@gmail.com",
  "potato@korea.com",
  "juha@gmail.com"
]
```
설명: Array 중 철자를 틀린 element를 찾는다. ```console.log(target)```으로 위치를 확인한 후 username을 가져온다.<br>
문자열을 @을 중심으로 쪼개고(split 키워드 사용) 첫번 째 파트만 가져온다.<br>
그 후 email을 수정한다. ```(friends[target] = `${username}@${email}`;)``` 마지막으로 target을 체크한다. 이 때 target은 존재하지 않게되어 -1을 반환한다.

-----------------------------------------------------------
### Array.fill()

array element를 지정 값으로 채운다.

ex)
```
const friends = [
  "tomato@korea.com",
  "pizza@gmail.com",
  "potato@korea.com",
  "juha@gmail.com"
];

friend.fill("*".repeat("5"), 1, 3); // 1은 시작값 3종료값

console.log(friends);

```
결과값 =``` [
  "tomato@korea.com",
  "*****",
  "*****",
  "juha@gmail.com"
]```
