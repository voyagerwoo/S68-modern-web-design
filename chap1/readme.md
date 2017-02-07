# CHAP1

## Graphics System
- 시각적인 시스템 - 컴퓨터는 점으로 그래픽을 표현한다.
- 점으로서의 속성 - x, y, width, height, color 등

#### 1. Fixed number
- 가장 기본적인 그래픽 표현 방법
- 업데이트가 정말 힘들다.

#### 2. Abstract Calculator
- context가 맞는 그래픽을 공유하고 싶다.
- screen size, chrome size, hierarchy calculator 를 기반으로
- %, top, block, inline, float => 추상화된 그래픽 표현

#### 3. Components System
- html tag - textarea, input, button, img, div

#### 4. Framework

## Rendering System
- 코드나 설계도 같은 눈에 보이지 않는 것들을 시각화
- 예를 들어, HTML 코드를 브라우저에서 시각화

#### 1. Geometric Calculator
- 코드를 공간(지형)을 계산하여 나눈다.
- Geometric = Layout

#### 2. Fragment Fill
- 나눈 공간 (픽셀)을 색으로 채운다.


## 책
#### 마크업의 시작
- 원고지의 꺽새에서 시작
- SGML -> HTML
- 그래서 html은 인쇄를 기술하는 언어
- html4에서 부터 문서에 의미를 알 수 있도록 의미를 갖는 태그를 추가하고 기존 태그에 의미 추가 (MS에서 사주)
- 오페라 만든 아저씨가 CSS 를 통해서 의미와 표현을 분리
- div와 span은 깍두기 - 의미를 안갖는 태그
- CSS를 잘 쓰게 되면 div 같은 깍두기를 점점 안쓰게 됨

#### 스타일의 시작
- 우선 HTML은 CSS를 모른다
- 스타일이 태그를 찾는 방법을 selector라고 함
- CSS 는 스타일과 selector의 조합 -> **rule**
- rule을 모아둔 것을 **ruleset** 이라고 함
- 여러가지 ruleset을 소유한 것을 sheet라고 함 -> **style sheet**
- 기본적으로 html은 기본 시트를 가지고 있다
- 기본 sheet를 덮어쓰고 가장 나중에 덮어쓴 것이 적용됨
- 스타일의 공통적인 부분을 클래스로 만든다.
- CSS는 기본적으로 부모 스타일 속성을 상속받는다. 이를 cascading 이라고 한다.
- CSS는 그래서 **Cascading Style Sheet** 이다.
- CSS는 긴 놈이 이긴다. 즉 더 구체적인 놈의 스타일이 적용된다. ex) .box2 < .boxA .box2

#### display
- **block** 은 (부모가 허용하는 한, 가능한 한) 가로 전체를 차지하는 것이다.
- **inline** 은 앞에 있는 요소의 baseline 같은 baseline을 갖고 ...
- 위 속성을 **display** 라고 한다.
- W3C에서 태그의 display 속성을 정의했다.

#### float
- 대부분의 개발자가 CSS를 공부했다가 포기하는 진입장벽
- 화면크기에 대응하는데 유용하다.
- float는 말 그대로 떠 있는 것(layer 개념). 그럼 안 떠있는 것은?
- 안 떠있는 것은 실체라고 하며, **Geometry 상에 공간을 점유** 하는 것
- float은 block과 inline에 영향을 주는 것이 다르다. 그래서 어렵다.
- **block 요소는 float 요소를 인식하지 못한다.**
- **inline 은 float 요소를 가이드/가드로 인식한다.**
- float라는 추상화된 시스템을 이해하고 제대로 사용하기 위해서는, 어떤 규칙으로 추상화를 구성했는지 이해해야 한다.
- float 끼리는 번호표를 줘야한다. **float들 끼리의 관계는 인라인** 처럼 보인다.



#### [주석]
- 영어 단어는 특정 상황에서 고유명사로서 의미를 갖는다.
- html의 장잠 : 텍스트 렌더링, form 랜더링
- 컴퓨터 과학은 공리가 없다. 그래서 다른 과학 분야보다는 쉽다.
- 디자인 할때 배치보다는 영역을 잡는다라는 표현이 더 알맞다.
- 프론트 개발의 불문률? id를 사용하지 않는다.
- 실력이 없을 수록 태그가 너무 많다.
