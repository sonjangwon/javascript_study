## JavaScript-HTMLElement

#### JavaScript-HTMLElement : 단수와 복수

> 객체를 제어하기 위해서는 객체를 찾아야 한다.

~~~HTML
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
  </head>
  <body>
    <ul>
      <li>HTML</li>
      <li>CSS</li>
      <li id="active">JavaScript</li>
    </ul>
    <script>
    var li = document.getElementById('active');
    console.log(li.constructor.name);   //HTMLLIElement
    var lis = document.getElementsByTagName('li');
    console.log(lis.constructor.name);  //HTMLCollection
    </script>
  </body>
</html>
~~~
>console.log(li.constructor.name); <br>
>return 값이 1개, 객체 1개의 이름을 알 수 있다.<br>
>document.getElementById : 리턴 데이터 타입은 HTMLLIELement<br>

>console.log(lis.constructor.name);<br>
>조회한 객체가 여러개, return 값이 여러개이다. <br>
>document.getElementsByTagName : 리턴 데이터 타입은 HTMLCollection<br>
>유사배열

> 즉 실행결과가 하나인 경우 HTMLLIELement, 복수인 경우 HTMLCollection을 리턴하고 있다. <br>

#### JavaScript-HTMLElement : HTMLElement

~~~HTML
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
  </head>
  <body>
    <a id="anchor" href="http://opentutorials.org">opentutorials</a>
    <ul>
      <li>HTML</li>
      <li>CSS</li>
      <li id="list">JavaScript</li>
    </ul>
    <input type="button" id="button" value="button"/>
    <script>
      var target= document.getElementById('list');
      console.log(target.constructor.name); //HTMLLIELement

      var target=document.getElementById('anchor');
      console.log(target.constructor.name); //HTMLAnchorElement

      var target= document.getElementById('button');
      console.log(target.constructor.name); //HTMLInputElement
    </script>
  </body>
</html>
~~~

> 각각의 태그명에 따라서 리턴 값이 달라진다.<br>
> 각각의 Element를 제어하기 위한 객체가 다르다. -> 기능이 다르다.<br>
> 공통의 태그 성격을 가지고 있지만(HTMLElement), 각각의 기능이 다르기 때문에 객체가 다르다.


- HTMLLIElement
~~~
interface HTMLLIElement : HTMLElement {
           attribute DOMString       type;
           attribute long            value;
};
~~~
- HTMLAnchorElement
~~~
interface HTMLAnchorElement : HTMLElement {
           attribute DOMString       accessKey;
           attribute DOMString       charset;
           attribute DOMString       coords;
           attribute DOMString       href;
           attribute DOMString       hreflang;
           attribute DOMString       name;
           attribute DOMString       rel;
           attribute DOMString       rev;
           attribute DOMString       shape;
           attribute long            tabIndex;
           attribute DOMString       target;
           attribute DOMString       type;
  void               blur();
  void               focus();
};
~~~

> 위는 모두 HTMLElement를 상속한다.<br>
> (객체가 다른 객체의 프로퍼티를 그대로 물려받으며, 자기 자신에게 필요한 기능을 추가한 것)<br>
> 부모 객체가 모두 HTMLElement, 동일한 부모객체의 기능을 가지고 있다.<br>
>

#### JavaScript-HTMLElement : DOM Tree

![](/picture/JavaScript-HTMLElement-1.png)

> 위에서 보이는 구조는 DOM Tree 구조이다.<br>
> HTMLElement 객체들의 부모는 HTMLElement이다..<br>
>그 부모는 Element이다..<br>
>최종 부모는 Node이다..<br>
