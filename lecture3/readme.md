# Lecture 3

1. Media Type
2. Display Area vs Device
3. Media Feature

참고 : https://developer.mozilla.org/ko/docs/Web/CSS/@media

## Media Type


## Media Feature
- width
- height
- orientation (portrait, landscape)
- aspect-ratio
- color
- monochrome
- scan : progresive | interlace
- grid : 0 | 1


## Media query apply
- link tag
```
<link rel="stylesheet" media="query" href="css"/>
```
- @media
```
@media query { rules }
```
- import
```
import url('xx.css') query
```


- 불필요한 것도 다 가져오는 비효율성이 있다.


### query 작성
- and 또는 or로 조건을 만든다.
- or == , (ex. screen, print == screen or print)
- and (ex. screen and resolution > 90dpi => 고해상도 이미지를 로드할지 여부를 확인할 때 사용 가능)
- 괄호 사용 가능, 괄호로 우선순위 적용


### Media query template
- **Mobile first template**

```
/* all */

/*mobile*/

@media (max-width=768px) {
  /*tablet portrait*/
}

@media (min-width=768px) and (max-width=1024px) {
  /*tablet*/
}

@media (min-width=1024px) {
  /*pc*/
}

```

## 주석
- 과제 : 책에 있는 그림만 보고 (css는 가리고) 코드를 작성해보자.
- device 보다는 display area를 기준으로 미디어 쿼리를 작성하자.
