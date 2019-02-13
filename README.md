# JavaScript
```
<script> </script> : JavaScript 를 html에서 쓰고 싶을 때 사용하는 태그
document.write : 화면에 표시하고 싶을 때 사용하는 javascript code

hi 버튼을 만들고 버튼을 누르면 경고창이 뜨도록 하고 싶음.
onclick property
1. value로 js코드가 와야 함
2. value를 html이 기억했다가 property에 해당하는 동작을 하면 value를 실행시킴

onchange property
: property에 해당하는 태그 안에서(ex: text) 무언가 변할 때

동작이 일어나는 것 : 이벤트(event)
구글에 이벤트 검색하고 싶을 때 : javascript xxx event

웹 브라우저에서 F12 -> Console 창에서 자바스크립트를 바로 실행시킬 수 있다

참고 링크 : https://developer.mozilla.org/ko/docs/Learn/JavaScript/First_steps/Variables

[데이터 타입] - 문자열과 숫자
https://developer.mozilla.org/ko/docs/Web/JavaScript/Data_structures
숫자 : ★연산★  
문자열 : "hello world"와 'hello world' 는 같음.
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String
위의 문서에서 string, number와 관련된 함수 등을 찾을 수 있으니 직접 찾아보자~

[변수]
var name = 'ny0011';
alert("fjijsdolfj  "+name+"ljwoejflojsd");
문자열에 변수값을 추가하고 싶으면 " + 변수이름 + " 요렇게 쓰자

[제어할 태그 선택]
1. body 태그 배경을 바꾸는 버튼 태그를 생성 : <input type="button" value="night">
2. 버튼을 눌렀을 때 배경이 변경되는 이벤트를 만들고 싶음 : onclick=""
3. JavaScript가 body태그를 찾는 방법을 알아보자 : javascript select tag by css selector
https://developer.mozilla.org/ko/docs/Web/API/Document/querySelector
4. JavaScript가 스타일을 변경하는 방법을 알아보자 : javascript element style
https://www.w3schools.com/jsref/dom_obj_style.asp
5. JavaScript가 배경색을 변경하는 방법 : javascript style background color
https://www.w3schools.com/jsref/prop_style_backgroundcolor.asp

[비교 연산자와 Boolean 데이터 타입]
=== : 이항 연산자. 오른쪽과 왼쪽값을 비교해서 같으면 True, 다르면 False
Boolean : true, false
html에서 <는 tag 예약어니까 &lt; 나 &gt; 를 써준다

[조건문]
if() {} else {}
() 안에 true, false 값을 갖는 비교 연산자나 Boolean 데이터 타입을 적는다.

[조건문의 활용]
버튼 하나로 배경을 바꾸고 싶음
1. 새 버튼을 만듦
2. onclick 이벤트에서 만약 현재 상태가 day면 night, night면 day로 바꾸고 싶음
3. 현재 상태를 가져오는 JavaScript 함수를 찾아보자 : javascript element get value
-> .value
-> 조건문 ()에 document.querySelector('#night_day').value 를 써주자
4. 한번 더 버튼을 누르면 실행이 안됨 -> value값도 버튼 누를 때 바꿔줘야 함

[리팩토링]
중복을 제거해보자!
1. document.querySelector('#night_day')는 태그 자기 자신을 가리키는 것과 같은 의미가 됨
-> 태그 자신을 가리키는 용어 : this
2. document.querySelector('body')는 4번이나 중복되어 나타남.
-> 변수를 써보자
var target = document.querySelector('body');

[배열]
검색 키워드
javascript array count
javascript array add data
https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Array

[반복문]
배열과 반복문이 같이 있을 때 서로의 효과가 두드러진다!
데이터 영역과 기능 영역을 분리할 수 있는 효과

[배열과 반복문의 활용]
a 태그 전부의 색을 바꿔보고 싶다
1. a 태그 전부를 검색하는 방법? javascript get element by css selector multiple
document.querySelectorAll()
2. 검색한 태그를 변수에 저장 -> Nodelist지만 배열처럼 사용할 수 있음
3. 변수에 저장된 alist[i]는 태그니까 태그의 색을 바꾸고 싶으면 .style.color 를 추가하면 됨.

[함수]
코드 중복이 여러 곳에서 반복문을 쓰기 어려운 상황에서 쓴다!
Parameter : 입력
return : 출력
-> 입출력을 설정해줘서 특정 기능만 수행하도록 코딩 가능

[함수의 활용]
지금까지 바꿨던 배경색 변경하는 코드를 함수에 넣어 다른 곳에서도 사용하고 싶음
1. function nightDayHandler() {}
2. 그런데 함수 안 this들은 그 함수가 있는 태그를 가리키니까 함수로 따로 빼면 작동하지 않음
-> 매개변수로 this값을 받도록 함
-> function nightDayHandler(self) {}
javascript의 this : https://k9e4h.tistory.com/141

[객체]
정보를 순서대로 저장하는 것 -> 배열
정보를 이름으로 불러서 꺼내는 것 -> 객체
key이름에 띄어쓰기가 들어가면 ""로 묶어서 배열처럼 정의하면 됨.
cowerkers["data scientist"] = "dd";
- 반복문 : javascript object iterate
https://stackoverflow.com/questions/14379274/how-to-iterate-over-a-javascript-object
- 메소드(method) : 객체에 소속된 함수
- 프로퍼티(property) : 객체에 소속된 변수
객체 자신을 가리키는 것 : this
cowerkers.showAll = function(){} // showAll이 cowerkers에 속해있기 때문에 showAll : 부분이 html에 출력됨

[객체의 활용]
중복되는 코드를 정리하기 위한 도구.
nightDayHandler 함수에서 중복되는 코드를 전부 함수로 만들고 나서 보니 이름들 설정하기 애매함
BodySetColor()
LinksSetColor()
-> setColor가 body인지 link인지 이름을 일일이 써줘야 할 수 있음
-> body와 link를 객체로 만들어보자!
Body.setColor()
Links.setColor()

[파일로 쪼개서 정리 정돈하기]
지금까지 작성한 js코드를 억개 페이지에 배포한다고 생각하면 수정 한번할 때마다 억번...
-> 코드를 파일로 만들자!
-> 파일 위치만 페이지에 복붙하면 끝

[library vs framework]
library : 재사용할 수 있는 sw. 가져와서 쓰는 느낌 ex) jQuery - cdn : https://developers.google.com/speed/libraries/#jquery
framework : 어떤 것(웹, 앱, 게임, ...)을 만들 때 공통적으로 필요한 부분만 모아둔 것. 프레임워크 안에서 기능 변경하는 느낌 ex)
cdn : script src로 링크로 library를 가져오는 기능. 다운로드 할 필요 없음
https://ko.wikipedia.org/wiki/%EC%BD%98%ED%85%90%EC%B8%A0_%EC%A0%84%EC%86%A1_%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC

[jQuery]
jQuery 구문 한 줄을 쓰면 jQuery가 대신 일 해줌!

```
<strong>reference : Coding Everyday(WEB2 - JavaScript, creator : egoing)</strong>
<p>
https://opentutorials.org/course/3085
</p>
<img src="https://s3-ap-northeast-2.amazonaws.com/opentutorials-user-file/module/3129/7333.jpg"></a>
