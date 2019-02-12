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


```
<strong>reference : Coding Everyday(WEB2 - JavaScript, creator : egoing)</strong>
<p>
https://opentutorials.org/course/3085
</p>
<img src="https://s3-ap-northeast-2.amazonaws.com/opentutorials-user-file/module/3129/7333.jpg"></a>
