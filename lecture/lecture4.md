# Position Model

- 지난 시간에 배웠던 Normal Flow : https://developer.mozilla.org/ko/docs/Web/Guide/CSS/Visual_formatting_model

- Normal Flow가 아닌것 : 지난 시간에 배웠던 float, 그런데 BFC에 소속된다.
- 그런데 position model을 쓰는 녀석들은 BFC에 소속되지 않는다.

### static
- disable - top, right, bottom, left, z-index

### relative
- 정상적인 normal flow 위치에 대해서 상대적으로 위치를 조절할 수 있다.
- normal flow에 잡힌 형태에서 위치만 이동됨
- 스크롤바는 이동한 위치만큼 생김, 즉 밀어서 부모의 크기가 늘어난다.
- **adjust only position**
- **enable offset parent**

### absolute
- 완전히 normal flow를 벗어남
- position이 non-static인 부모 엘리먼트(relative, absolute, fixed)를 기준으로 위치를 잡는다.
- 부모중에 non-static인 부모 엘리먼트가 없으면, root container(html에서 body)를 기준으로 위치를 잡는다.

## fixed
- viewport(display-area) bound 를 기준으로 위치를 잡는다.
- 즉 현재 보이는 화면의 기준으로 부터 위치를 잡는다.
- iframe에도 들어갈 수 있다.

## sticky
- 항상 특정 위치에 붙어있는 position model
- IE 빼고 웬만한 브라우저는 지원되는 기능
- 부모 컨테이너가 화면에 있을 때 까지만 sticky가 적용된다. - 부모와 공동 운명체
- 본인이 스크롤 한계에 도달하지 않으면 그냥 normal flow, 스크롤 한계를 넘으면 fixed
- top : -1px => 1px짜리 border를 안보기 위해서 넣은 코드, 위로 1px 올림
- 일반적으로 sticky는 top만 구현해놨다고 한다. 다른 것(left, right, bottom)은 협의 중 (https://drafts.csswg.org/css-position-3/#sticky-pos)
- sticky 안에 sticky가 가능하다
- sticky sample :  http://semantic-ui.com/examples/sticky.html

## Relative Bridge
- 보통의 화면은 normal flow로 나타나는데 특정 박스는 맘대로 배치하고 싶을 때 해당 영역의 position을 relative로 하고 자식들을 absolute로 하여 구성한다.


## 숙제
- width vs left, right


# 책 내용
- 2장은 컴포넌트를 준비하는 단계

## encoding vs decoding
- 단지 표현을 바꿔주는 것
- 주소에 한글을 치면 %~ 이런 식으로 표현이 변경된다. 언제든 다시 한글로 바꿀 수 있다.
- UTF-8은 유니코드를 사용하는 코드 변환기
- 문자 -> 유니코드 -> 숫자 -> UTF-8/16/32 방식으로 인코딩


### 주석
- absolute는 실체가 아니다.
- 법칙 : 프로그램은 무조건 변경된다.
- 그 법칙 때문에 격리한다...
- scaffolding뼈대를 잡는다
