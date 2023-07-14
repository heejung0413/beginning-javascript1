# -

<h3> 5장 정리 </h3>
https://github.com/heejung0413/beginning-javascript1/blob/main/05/read.md
</br>
<h1> 05. 함수와 이벤트 👋 </h1>
<h2>05-1 여러 동작을 묶은 덩어리, 함수 </h2>

<br/> 

	< button onclick="addNumber()"> 덧셈 계산하기 < /button>

<br/> - onclick은 버튼을 눌렀을 때 실행할 대상인 함수를 알려주는 예약어
    <br/>

    function addNumber() {
    var sum = 10+20;
    alert(sum);
    }
- alert();
 경고창 띄우기
<br/>

 <h2>05-2 let과 constant로 변수 선언하기  </h2>

<h3> 지역변수</h3>

- 한 함수에서만 사용할 수 있는 변수

<h3> 전역 변수</h3>
- 스크립트 소스 전체에서 사용할 수 있는 변수
- 변수를 한 번 선언하면 그 값이 계속 유지된다는 뜻
- 함수 안에서 새롭게 변수를 선언하려면 변수 이름 앞에 var 예약어를 사용하지 않아도 된다.

<h3> let 변수</h3>
- var과 constant, let 의 차이는 스코프범위(let을 더 이용하는 것이 좋다). var는 함수 영역의 스코프를 가지지만 let과 constant는 블록 영역의 스코프
- 블록에서만 쓸 수 있는 변수: let
-선언하기 전에 사용할 경우, 오류

<h3> constant 변수</h3>
- 변하지 않는 값 선언할 때 사용 -> 재선언 X 재할당 X
- 블록 레벨 스코프

<h3> ⚠ 변수 사용방법 ⚠</h3>
- 전역변수를 최소화 하기
- var 변수는 시작 부분에서 선언
- for문에서 카운터 변수를 사용할 때는 블록 변수를 사용하면 편리!

ex)

    var i;
    for(i=1; i<=n; i++){ ...

</br>

 <h2>05-3 여러번 사용할 수 있는 함수 만들기  </h2>
 <h3> 매개변수 </h3>
 
 - 함수를 실행하기 위해 필요하다고 지정하는 값 -> '입력'이라고 생각
 - 인수: 함수를 실행할 깨 매개변수로 넘겨주는 값

</br>

     function addNumber(a, b) { 			
    var sum = a + b;
    return sum;
    }
- a,b는 매개변수에 인수 넣은 것 

</br>

    var num1 = parseInt(prompt("첫 번째 숫자 : "));
    var num2 = parseInt(prompt("두 번째 숫자 : "));
    var result = addNumber(num1, num2);
    alert("두 수를 더한 값은 " + result + "입니다.");

    function addNumber(a, b) { 			
    var sum = a + b;
    return sum;
    }
</br>

 <h2>05-4  함수 표현식  </h2>

 - 함수를 선언한 후 함수 이름을 사용해 실행하는 것이 기본 방법이지만, 이외에도 함수를 실행하는 방법이 있다. 그것이 '함수 표현식'
 <h3> 익명 함수 </h3>
 
 - 이름을 붙이지 않은 함수 
 - 함수 자체가 식이기 때문에, 익명함수를 변수에 할당할 수 있음

 </br>

    var sum = add(10, 20); //익명함수 실행 후 결괏값을 변수 sum에 저장
    sum
    30

 <h3> 즉시 실행 함수 </h3>

- "정의함"과 동시에 "실행"되는 함수

</br>
    
    var result = (function (a,b) { //매개변수 추가
        return a+b; 
    } (10,20)); //인수 추가
    console.log(result);
    30

 <h3> 화살표 함수 </h3>

- 매개변수가 없을 때

</br>

    const hi = () => "안녕하세요?";

- 매개변수가 1개일 때

</br>

    let hi = user => { document.write (user + "님, 안녕하세요?"); }

- 매개변수가 2개 이상일 때

</br>

    let sum = (a, b) => a + b;

 <h2> 05-5  이벤트 다루기  </h2>

 실습:
 https://heejung0413.github.io/beginning-javascript1/05/event-handler.html
</br> https://heejung0413.github.io/beginning-javascript1/05/event.html
</br> https://heejung0413.github.io/beginning-javascript1/05/event-dom.html
 
