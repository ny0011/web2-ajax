
# Ajax
전체 페이지를 다시 불러오지 않고 웹서버에 정보를 요청해 부분적으로 정보를 갱신

```
[fetch API 기본 사용법]

fetch('html').then(function(response){
        response.text().then(function(text){
          alert(text);
        })
})
폴더 내에 html 파일을 찾고(fetch())
그 결과를 받아서(response)
파일 내용(text)을 경고창으로 출력(alert())

[fetch API의 요청과 응답]

function callbackme(){
    console.log('response end');
}

fetch('html').then(callbackme);
console.log(1);
console.log(2);

fetch('Javascript') : Javascript라는 파일을 찾아달라고 client가 server에게 요청
.then(callbackme) : server에게 응답을 받으면 callbackme함수를 실행시킨다
--> console에서 log 결과는 서버에게 응답 받기 전까지 client의 명령을 수행함(1,2가 먼저 찍힘)
--> server에게 응답 받으면 'response end'가 log에 찍힘
--> asynchronous(비동기) : server 응답을 기다리지 않고 실행됨

for문으로 console.log를 1000번쯤 찍으니 다 찍을 때까지 기다리고 'response end'가 실행되는듯...

[fetch API - response 객체]
fetch('html').then(function(response){})에서 function(response){}는 익명함수!

callbackme = function(){};
fetch('html').then(callbackme); 와 같은 의미임

function(response){}가 호출될 때 response를 매개변수로 함.
response는 뭘까?
response 객체의 속성값들이 들어있는데 그 중 status = 200인 것이 있음
server가 정상적으로 파일을 찾았으면 200을 보냄(ok)
server가 못찾으면 404를 보냄(not found)

[Ajax의 적용]
제목을 클릭하면 x.html 페이지로 새로 이동하는 것이 아니라 파일을 불러와서 현재 페이지에 보여줌.

[리팩토링 - 함수화]
코드 중복이 발생함! 리팩토링 ㄱㄱ

중복이 발생하는 코드를 함수로 묶고 페이지마다 다른 값을 가지는 것을 변수로 설정

[초기 페이지 구현]
- 문제점
1. 링크표시가 없음
2. 클릭해야 내용이 보임
=> 해쉬(북마크) 기능을 쓰자

내가 가리키고 싶은 태그에 id 값을 주면 링크로 그 위치를 찾을 수 있다
=> id를 fragment identifier라고도 부름.
=> id값으로 링크 위치를 표시
http://127.0.0.1:81/hash.html#three

링크를 찾을 때 a href를 사용함
<a href="#three">three</a>

url에서 #에 해당하는 값을 javascript에서 찾고 싶을 때?
https://stackoverflow.com/questions/298503/how-can-you-check-for-a-hash-in-a-url-using-javascript

#three에서 three만 떼어내고 싶을 때?
문자열 조각을 substring이라고 부름
how to get substring in javascript
https://www.w3schools.com/jsref/jsref_substring.asp

- 적용
a href="#!html" => 해시 기능을 쓸 때 #!라고 붙임. hash bang(?)
만약 http://127.0.0.1:81/index.html#!html 링크로 페이지에 접근했을 때 바로 html 내용을 보고 싶으면?

- 문제점
1. 검색엔진 최적화가 안됨
-> 백엔드에서 동적으로 가져옴.
-> 내용을 볼 수 없음
2. navigation(페이지 이전←, 이후→ 가져오기)를 했을 때 페이지 리로딩이 안됨
-> pjax가 새로 나옴

[글목록 ajax로 구현하기]
- 문제점
1. index.html에서 data와 기능이 함께 구현되어 있음
data : 바뀔 수 있는 부분 -> html, css, javascript 글 목록
-> 페이지가 로딩될 때 글 목록을 불러오기
☆ index.html에 있던 내용들은 파일로 만들어지고 그 내용이 들어갈 껍데기만 남음! 싱기
index를 수정하지 않고 내용 파일만 수정하면 됨.




```


<strong>reference : Coding Everyday(WEB2 - Javascript - Ajax, creator : egoing)</strong>
<p>
https://opentutorials.org/course/3281
</p>
<img src="https://s3-ap-northeast-2.amazonaws.com/opentutorials-user-file/module/3129/7333.jpg"></a>
