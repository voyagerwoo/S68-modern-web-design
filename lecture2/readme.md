# Lecture 2

## 목차
1. Box Model
2. Normal Flow
3. Display & Float


##  Box Model
>margin - 밖 여백   
>border - 경계선  
>padding - 내부 여백  
>contents - 내용물

- 아무 설정도 하지 않았을 때 width, height는 contents의 width, height
- box-sizing 이라는 옵션으로 box model을 설정 (border-box, padding-box, 등)

## Normal Flow
- Normal flow란, html이 렌더링할 때, static position model 내에서 그림을 그리는 방법이다.
- static-model : (정적이라는게 아니고) 컴퓨터가 알아서 그린다.
- block : 세로로 배치하는 행위
- inline : 가로로 배치하는 행위
- BFC(Block Formatting Context) : 세로로 배치하는 컨택스트 (ex. Body tag)
- IFC(Inline Formatting Context) : 가로로 배치하는 컨택스트. block 엘리먼트를 만들 때 그 내부는 IFC가 발동된다.
- 이런 걸 layering, 계층화 라고 한다.

#### BFC
https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Block_formatting_context
> A block formatting context is created by one of the following:
- the root element or something that contains it
- floats (elements where float is not none)
- absolutely positioned elements (elements where position is absolute or fixed)
- inline-blocks (elements with display: inline-block)
- table cells (elements with display: table-cell, which is the default for HTML table cells)
- table captions (elements with display: table-caption, which is the default for HTML table captions)
- block elements where overflow has a value other than visible
- flex boxes (elements with display: flex or inline-flex)
- display: flow-root  



BFC containing
- 자식 엘리먼트는 모두 포함된다.
- 새로운 BFC의 자식 엘리먼트는 포함하지 않는다.


## Display & Float
- display-outside : 외부 입장에서 나의 영역에 대한 설정, block, inline, inline-block
- display-inside : 내부 입장에서 나의 영역에 대한 설정, table, flex, grid
- display-internal : table-cell
- inline의 크기는 wrap content로 설정된다.
- float 박스의 위치는 BFC박스의 좌상단을 기준으로 결정된다.
- float 끼리는같은 레이어를 공유하고 있다.
- **pseudo** : 그 의미를 나타내고 있지만 대체가능하다, 가짜지만 진짜인 경우, 진짜는 아니지만 존재함
- **pseudo element** : 오직 그림 그리기 위한 element. 그래서 메타 정보가 전혀 없다. 그리고 pseudo element 만이 content 속성을 가지고 있다. 그래픽적인 효과를 주기 위해서 쓰인다.
 (:after, :before, 등)
- float 속성인 element는 display:inline 이라고 해도 block으로 환원된다.
- float 속성은 width가 기본적으로 auto 이다.
- float 에서 컬럼탈락에 주의할 점은 엘리먼트의 높이가 다를 경우이다.
- float 정렬이란?? 남는 공간에 잘 끼워넣는다.






### 주석
- **모든 단어는 고유명사**
- 개발 실력은 외우는 것으로 결정된다. (머리로 하는 것 아니다.)
- 잘 외워서 체계적으로 정리하고, 꾸준히 업데이트를 해줘야지 실력이 는다.
- 쳬계적이지 않은 지식은 붕괴하기 쉽상
- http와 브라우저를 처음 만들고 넷스케이프를 만든 **마크 앤드리슨**
- 자바스크립트를 만든 **브랜든 아이크**
- reflow : geometric을 갱신하여 영역을 다시 계산하고 다시 그릴 때
- repaint : geometric의 변화가 아닌 그냥 픽셀 단위의 색깔만 변경
- 원리는 단순히 스펙을 차근차근 알고 있는냐에 달려있다.
- 소숫점은 최근 브라우저에서는 소수점 16자리까지 인식한다.
- 지금 예제는 인라인 또는 인라인 블록으로 대체가능하지만, 나중에 반응형 웹을 위해서 float을 연습하고 있다.
### 참고
- https://developer.mozilla.org/ko/docs/Web/Guide/CSS/Block_formatting_context
- https://developer.mozilla.org/ko/docs/Web/CSS/clear
