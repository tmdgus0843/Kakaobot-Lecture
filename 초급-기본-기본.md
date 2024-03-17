안녕하세요, Yellu에요!

오늘은 카카오톡 봇을 만드는데 필요한 기본 용어들을 알아볼게요!

---

먼저 봇 앱을 켜서 봇을 생성하고 코드 편집에 들어오면 아래와 같은 코드가 보일거예요.

```javascript
//메신저봇R / 채팅 자동응답 봇 //레거시 API 기준 
function response(room, msg, sender, isGroupChat, replier, ImageDB, packageName) {

}
```
위는 함수(function)로 앞으로 많이 보게될 친구예요.

위 함수는 우리가 카톡 메시지 알림이 올때마다 작동해요.

그럼 함수옆에 ()는 뭐냐고요?

()안에 있는 친구들은 매개변수(parameter)라 해요.

이때 변수는 말 그대로 변수(변하는 수)예요.

상수는 변하지 않는 수를 말하죠.

우린 이 매개변수와 변수로 프로그래밍을 할거예요.

그럼 찬찬히 살펴볼게요.

```
room : 채팅방의 이름을 담고 있어요. 
msg : 채팅방에서 온 메시지를 담고 있어요. 
sender : 채팅방에서 메시지를 보낸 사람의 이름을 담고 있어요. 
isGroupChat : 메시지가 온 채팅방이 그룹채팅인지 확인해요. 
replier : 이 변수로 답장을 해요. 
ImageDB : 프로필 해시코드 등을 담고 있어요. 
packageName : 메시지가 온 앱의 패키지명을 담고 있어요.
```

그럼 이제 메시지를 받고 답장을 보내볼게요.

먼저 기본 함수를 적어줘요.

```javascript
function response(room, msg, sender, isGroupChat, replier, ImageDB, packageName) {

}
```

그런 다음 {}안에 replier를 넣어 볼게요.

이때 replier은 혼자 놀지 못해서 친구를 붙여줘야 해요.

그래서 replier뒤에 reply를 붙여줄게요.

그런 다음 ()를 붙여 안에 보낼 말을 입력해볼게요.

이때 보낼 말은 ''(따옴표), ""(쌍따옴표)를 써야해요.

그리고 각 코드가 끝날 때 마다 ;(세미콜론)을 붙여줘야 해요.

안붙여도 작동은 하지만 붙여주는게 좋아요.

```javascript
function response(room, msg, sender, isGroupChat, replier, ImageDB, packageName) {
  if (msg == "!테스트") {
    replier.reply( 
      "방 이름 : " + room + "\n" + 
      "보낸사람 이름 : " + sender + "\n" + 
      "메시지 내용 : " + msg 
    );
  }
}
```

이렇게 한 다음 리로드 해볼게요.

이제 작동시켜 볼까요?

디버그룸에 들어가 볼게요.

![image](https://github.com/tmdgus0843/Kakaobot-Lecture/assets/120067908/5972ccde-fcbf-4cf1-a74c-280613493ca0)


오

실행이 돼네요!

그러면 이제 소스를 해석해볼게요.

아 참고로 `//`는 JS에서 주석으로 처리돼요.

주석은 아래와 같이 각 코드에 대한 설명을 적거나 하는 용도로 사용돼요.

아 이때 주석처리된 코드는 작동하지 않아요.

```js
function response(room, msg, sender, isGroupChat, replier, ImageDB, packageName) {
  if (msg == "!테스트") { //이 줄은 if문으로 [if문과 연산자] 강의에서 다룰게요! 
    replier.reply( //"!테스트" 라는 글자에 대답해요. 
      "방 이름 : " + room + "\n" + //"방 이름 : "이라는 글자 뒤에 매개변수 room을 불러와 더해요. 
      "보낸사람 이름 : " + sender + "\n" + //"보낸사람 이름 : "이라는 글자 뒤에 매개변수 sender을 불러와 더해요. 
      "메시지 내용 : " + msg //"메시지 내용 : "이라는 글자 뒤에 매개변수 msg을 불러와 더해요. 
    );
  }
}
```

오늘 사용한 코드는 위와 같이 해석할 수 있어요.

---

다음 강의에는 'if문과 연산자'로 돌아 올게요~!

다음 강의에서 만나요~~
