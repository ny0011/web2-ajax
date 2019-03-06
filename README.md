
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


```


<strong>reference : Coding Everyday(WEB2 - Javascript - Ajax, creator : egoing)</strong>
<p>
https://opentutorials.org/course/3281
</p>
<img src="https://s3-ap-northeast-2.amazonaws.com/opentutorials-user-file/module/3129/7333.jpg"></a>
