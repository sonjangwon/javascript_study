## JavaScript-HTMLCollection

> HTMLCollection은 리턴 결과가 복수인 경우에 사용한다.
> HTMLCollection의 목록은 실시간으로 변경된다.
> Element의 List를 담은 결과를 HTMLCollection에 담았다.

~~~html
console.group('before');
var lis = document.getElementsByTagName('li');
for(var i =0; i<lis.length;i++){
    console.log(lis[i]);
}
console.groupEnd();

//lis는 HTMLCollection
~~~



> Console.group('before')으로 console을 묶을 수 있다.
> console.groupEnd()으로 종료.



~~~html
list[1].ParentNode.removeChild(list[1]);
~~~

> lis의 변수에 담겨있는 HTMLCollection의 1번째 Element를 삭제한다.
> 제거된 순간에 바로 반영되기 때문에 List를 재조회하지 않아도 된다.
