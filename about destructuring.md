#### object destructuring 
큰 오브젝트에서 특정 변수나 그 안에 속한 작은 오브젝트에 접근할 수 있도록 해준다.
<br>
예제
```
const settings = {
  notifications: {
    follow: true,
    alerts: ture,
    unfollow: false
  },
  color: {
    theme: "dark"
  }
};
//위와 같은 오브젝트가 있을 때,
  notifications 를 불러오는 방법은 다음과 같다.

const {
  notifications
} = settings;

//=settings; 가 의미하는 바는 
//const notifications = settings.notifications 이다.
//nofifications는 const 변수
```
---------------------------------------------------------------
#### array destructuring

예제
```
const days = ["mon","tue","wed"];

const [mon, tue, wed, thu = "thu"] = days;

//default velue로 없는 값을 생성할 수 있다. 
```
------------------------------------------------------------------
#### function destructuring

변수의 가독성을 높여주고, 각 변수의 기본값을 설정해줄 수 있다.
```
function saveSettings({ notifications, color: { theme} }) {
  console.log(color);
}

saveSettings({
  follow: true,
  alert: true,
  mkt: false
},
  color: {
    theme: "blue"
  } 
});
```
