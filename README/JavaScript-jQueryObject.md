## JavaScript-jQueryObject

#### JavaScript-jQueryObject : 특성

![](/picture/JavaScript-jQueryObject-1.png)

>암시적 반복<br>
>jQuery객체에서는 암시적인 반복이 수행된다. 즉, 내부적으로 반복문을 우리 대신에 수행한다.

~~~
li.css('text-decoration','underline');
~~~
>위와 같이 인자가 2개인 경우는 css설정을 한다는 내용이다.<br>
>li의 element의 text-decoration을 underline한다는 내용이다. <br>

~~~
li.css('text-decoration');
~~~
>하지만 다음과 같이 인자가 1개인 경우는 값을 가져온다는 내용이다.<br>
>이 때 가장 맨 첫번째로 등장하는 li의 인자값만 가져오게 된다.

>체이닝<br>
>chaining이란 선택된 엘리먼트에 대해서 연속적으로 작업을 처리할 수 있는 방식이다.

#### JavaScript-jQueryObject : 엘리먼트 정보

>jQuery함수를 이용해 가져온 객체는 유사 배열이라서 배열과 같은 방법으로 제어가 가능하다.<br>
>li자체에 담겨있는 값은 jQuery Object이다.<br>
>li[i].constructor 했을 때 그 안에 담긴 값은 jQuery객체가 아니라 DOM객체이다.<br>

![](/picture/JavaScript-jQueryObject-2.png)

>다시 jQuery 객체로 만들어주면 된다.
~~~
$(li[i]).css('color', 'red');
~~~
>CSS 선택자에 해당하는 $('li')가 jQuery객체를 리턴한다.

![](/picture/JavaScript-jQueryObject-3.png)
>위의 내용은 DOM 객체를 리턴 한 것이고 아래는 jQuery 객체를 리턴한 것이다.


#### JavaScript-jQueryObject : .map()

~~~html
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
  </head>
  <body>
    <ul>
     <li>html</li>
     <li>css</li>
     <li>JavaScript</li>
   </ul>
   <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
   <script>
       var li = $('li');
       li.map(function(index, elem){
           console.log(index, elem);
           $(elem).css('color', 'red');
       })
   </script>
  </body>
</html>
~~~
>map함수<br>
~~~
function(index,elem)
~~~
>index에는 element값이 전달되고,elem에는 DOM Object값이 전달된다.<br>

![](/picture/JavaScript-jQueryObject-4.png)
>위의 결과에서 0,1,2는 element이고 li는 DOM Object이다.<br>
>그리고 뒤의 DOM 객체를 jQuery 형식으로 감싸서 css메소드를 사용한다.

#### JavaScript-jQueryObject : API

>API = Application Program Interface<br>
>
>https://api.jquery.com 에서는 우리가 쓸 수 있는 API가 나와 있음.<br>

>예제를 살펴보면서 이것을 어디다 쓰는지 이해해야 한다.<br>
>css라는 메소드를 이용해서 element의 어떤 값을 세팅하는 것에 대한 방법이 나온다.<br>
![](/picture/JavaScript-jQueryObject-5.png)
>css 메소드에서 앞의 속성에 대한 값을 뒤의 인자로 변경 시킨다.<br>
>API 보는 법을 익숙해지고, 반복적으로 사용하다보면 jQuery를 사용할 수 있는 방법을 알게 될 것이다.<br>
