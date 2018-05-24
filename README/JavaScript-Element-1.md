## JavaScript-Element

#### 식별자 API

- Element.tagName
>
~~~html
<li id="active" class="important current">JavaScript</li>
document.getElementById('active')
~~~
>위의 부분은 HTMLLIElement라는 객체를 갖는다.<br>
>HTMLLIElement은 HTMLElement와 Element를 상속받는다. <br>
>Element에는 tagName이라는 프로퍼티가 있다.<br>
>이를 이용하면 Element의 Tag이름을 알 수 있다.<br>
>TagName 은 읽기 전용이다. 중간에 마음대로 바꿀 수 없다.<br>


- Element.id
>ID는 문서에서 단 한번만 등장 할 수 있는 식별자이다.<br>
>각각의 엘리먼트에서 단 하나만 식별한다.<br>
>같은 이름을 가지고 있는 태그는 존재하지 않는다.<br>
>아래의 코드는 id를 변경하는 코드이다.
>
~~~
<ul>
    <li>html</li>
    <li>css</li>
    <li id="active">JavaScript</li>
</ul>
<script>
var active = document.getElementById('active');
console.log(active.id);
active.id = 'deactive';
console.log(active.id);
</script>
~~~

- Element.ClassName
~~~
<ul>
    <li>html</li>
    <li>css</li>
    <li id="active">JavaScript</li>
</ul>
<script>
var active = document.getElementById('active');
// class 값을 변경할 때는 프로퍼티의 이름으로 className을 사용한다.
active.className = "important current";
console.log(active.className);
// 클래스를 추가할 때는 아래와 같이 문자열의 더한다.
active.className += " readed"
</script>
~~~
>class는 자바스크립트의 예약어이기 때문에 className이라는 명칭을 쓴다.<br>
>className은 추가,삭제할 때 불편하다.
>그래서 classList를 사용한다.

- Element.classList
>편리한만큼 사용하기 까다롭다.
>
~~~
<ul>
    <li>html</li>
    <li>css</li>
    <li id="active" class="important current">JavaScript</li>
</ul>
<script>
function loop(){
    for(var i=0; i<active.classList.length; i++){
        console.log(i, active.classList[i]);
    }
}
// 클래스를 추가
</script>
<input type="button" value="DOMTokenList" onclick="console.log(active.classList);" />
<input type="button" value="조회" onclick="loop();" />
<input type="button" value="추가" onclick="active.classList.add('marked');" />
<input type="button" value="제거" onclick="active.classList.remove('important');" />
<input type="button" value="토글" onclick="active.classList.toggle('current');" />
~~~
>실무적인 기능으로 이 기능에 대한 필요성을 느끼기 전까지는 지루함을 느낄 수 있다.<br>
>띄어쓰기를 기준으로 클래스의 Name의 Length를 구분한다.
>active.classList
>class가 여러개 있을 경우 모든 class를 담아놓는 객체(띄어쓰기로 구분)<br>
>
>active.classList.add('important');
>active.classList.remove('important');
>active.classList.toggle('important'); (존재하면 삭제하고 없으면 추가시킨다.)
