# trim, trimStart,trimEnd

비어있는 공간을 잘라준다. 
form 같은 형식이 있을 때 유용하다.

trim 은 양쪽 모두의 여백을 잘라준다.
trimEnd 는 문자열 끝부분의 여백을 잘라준다.
trimStart 는 문자열 앞부분의 여백을 잘라준다.
ex)
```
("    name").trimStart

//결과값 "name"

("name      ").trimEnd

//결과값 "name"

("    name      ").trim

//결과값 "name"
```
