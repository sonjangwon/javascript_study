## JavaScript-Element

> li의 element는 HTMLLIElement  (li가 특히 가질 수 있는 속성)<br>
> 이것의 부모는 HTMLElement  (HTML이 특히 가질 수 있는 속성)<br>
> 이것의 부모는 Element  (모든언어가 가질 수 있는 속성)<br>

> Element는 모든 element에 대한 공통적인 기능을 담고 있다.

### 주요기능
- 식별자<br>
문서 내에서 특정한 엘리먼트를 식별하기 위한 용도로 사용되는 API
  + Element.classList
  + Element.ClassName
  + Element.id
  + Element.tagName

- 조회<br>
엘리먼트의 하위 엘리먼트를 조회하는 API
  + Element.getElementsByClassName
  + Element.getElementsByTagName
  + Element.querySelector
  + Element.querySelectorAll

- 속성<br>
엘리먼트의 속성을 알아내고 변경하는 API
  + Element.getAttribute(name)
  + Element.setAttribute(name,value)
  + Element.hasAttribute(name)
  + Element.removeAttribute(name);
