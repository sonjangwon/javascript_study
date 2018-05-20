
## javaScript-jQuery 제어 대상 조회하기

#### javaScript-jQuery 제어 대상 조회 : 기본문법

>jQuery의 기본 문법은 단순하고 강력하다<br>
>$('li').css('color','red');
>
>항상 $로 시작한다. $는 jQuery function이다.<br>
>$ 다음 인자는 Css Selector가 들어온다.<br>
>jQuery function이 return한 어떠한 객체는 jQuery 객체이다.<br>
>jQuery의 element 중 li  전체에 대해서 css라는 메소드를 실행한다.<br>
>color를 red로 변경한다.<br>
>li style="color:red"와 동일하다.<br>

#### javaScript-jQuery 제어 대상 조회 : 엘리먼트 1

![](/picture/javaScript-jQuery 제어 대상 조회하기-1.png)

>jQuery로 헀을 때는 1줄, DOM으로 코딩하면 3~4줄<br>
>DOM은 반복문을 하나 씩 돌면서 값 변경<br>
>jQuery는 li에 해당하는 모든 element에 대하여 한 번에 값 변경.<br>


#### javaScript-jQuery 제어 대상 조회 : 엘리먼트 2

>.active는 클래스 이름이 active인 것들.

#### javaScript-jQuery 제어 대상 조회 : 엘리먼트 3

>DOM에서는 li.style이라는 부분이 중복적으로 사용된다.<br>
>jQuery는 1줄에 연속적으로 메소드를 호출해서 작업이 가능하다.<br>
>#active는 ID 값이 active인 것들을 가르킨다.<br>
>앞의 css메소드의 return한 값에서 css메소드를 실행시킨다.(Chaining) 
