- HTML로 문서를 이쁘게 하기엔 한계가 있다
- CSS를 사용해 스타일링 가능

# CSS

- Cascading Style Sheets : HTML 등의 마크업 언어로 작성된 문서가 실제 웹사이트에 표현되는 방법을 정해주는 스타일 시트 언어
    - Cascading : 계단식 → 우선순위의 따라 스타일 규칙이 적용

# Selector (선택자)

## 인라인 스타일

```html
<body>
    <h1 style="
        color: yellow;
        background-color: red;
    ">신짱구</h1>
    <p> 안녕하세요. 저는 떡잎마을에 사는 신짱구입니다. 5살이에요.</p>
```

- 인라인 스타일 : 태그에 직접 스타일을 입히는 방식
- 태그에 style 속성을 통해 구현

## 내부 스타일 (임베딩 스타일)

```html
<head>
	<title>Hello</title>
	<style>
		h1, h2, h3, h4, h5, h6 {
			color: yellow;
			background-color: red;
		}
	</style>
</head>
```
- 파일 내 모든 h 태그에 한번에 적용 가능
- head 태그 내부에 style 태그로 정의
- 전체 선택시 셀렉터를 *로 표시
- id, class, 속성 값을 사용할수도 있다

## 외부 스타일 (링크 스타일)

```css
// style.css 파일 //

h1, h2, h3, h4, h5, h6 {
    color: red;
    background-color: yellow;
}
```

```html
// index.html 파일 //

<head>
	<title>Hello</title>
	<link rel="stylesheet" href="./style.css">
</head>
```

- 모든 파일에 한번에 적용 가능
- HTML 문서와는 별개의 파일에서 스타일을 지정
    - 스타일을 한번에 작성하여 여러 HTML문서에 적용 → 유지보수 용이

## 우선순위

- 인라인 스타일 > 내부 스타일 > 외부 스타일

# 색상 정의

- RGB or hexcode

## Class

```css
// style.css 파일 //

.zzang {
    color: red;
    background-color: yellow;
}
```

```html
<!DOCTYPE html>
<html>
<head>
    <title>Hello</title>
    <link rel="stylesheet" href="./style.css">
</head>
<body>
    <h1 class="zzang">신짱구</h1>
    <p>안녕하세요. 저는 떡잎마을에 사는 <span class="zzang">신짱구</span>입니다. 5살이에요.</p>
    <h2>
        가족 관계
    </h2>
    <p>엄마, <a href="./father.html">아빠</a>, <span class="zzang">저</span>, 동생. 그리고 흰둥이와 함께 살아요.</p>
</body>
</html>
```

- <span>신짱구</span> : 범위, 공간, 간격 의미의 태그
- 짱구를 지칭하는 단어를 하나의 class로 묶는다
- 태그가 아님 → 선택자를 점(.)으로 시작하면 class
    - zzang이라는 클래스 집단

# 크기 단위

## px (픽셀)

## % (백분율)

## em (배수)

# Box 영역

| 명칭 | 설명 |
| --- | --- |
| Content | 요소의 텍스트나 이미지 등의 실제 내용이 위치하는 영역이다. width, height 프로퍼티를 갖는다. |
| Padding | 테두리(Border) 안쪽에 위치하는 요소의 내부 여백 영역이다. padding 프로퍼티 값은 패딩 영역의 두께를 의미하며 기본색은 투명(transparent)이다. 요소에 적용된 배경의 컬러, 이미지는 패딩 영역까지 적용된다. |
| Border | 테두리 영역으로 border 프로퍼티 값은 테두리의 두께를 의미한다. |
| Margin | 테두리(Border) 바깥에 위치하는 요소의 외부 여백 영역이다. margin 프로퍼티 값은 마진 영역의 두께를 의미한다. 기본적으로 투명(transparent)하며 배경색을 지정할 수 없다. |

## block 레벨 요소

- block 특성 요소의 특징
    - 항상 새로운 라인에서 시작한다.
    - 화면 크기 전체의 가로폭을 차지한다. (width: 100%)
    - width, height, margin, padding 프로퍼티 지정이 가능하다.
    - block 레벨 요소 내에 inline 레벨 요소를 포함할 수 있다
    - block 레벨 요소
        - div
        - h1 ~ h6
        - p
        - ol
        - ul
        - li
        - hr
        - table
        - form

## inline 레벨 요소

- 새로운 라인에서 시작하지 않으며 문장의 중간에 들어갈 수 있다. 즉, 줄을 바꾸지 않고 다른 요소와 함께 한 행에 위치한다.
- content의 너비만큼 가로폭을 차지한다.
- width, height, margin-top, margin-bottom 프로퍼티를 지정할 수 없다. 상, 하 여백은 line-height로 지정한다.
- inline 레벨 요소 뒤에 공백(엔터, 스페이스 등)이 있는 경우, 정의하지 않은 space(4px)가 자동 지정된다.
- inline 레벨 요소 내에 block 레벨 요소를 포함할 수 없다. inline 레벨 요소는 일반적으로 block 레벨 요소에 포함되어 사용된다.
- inline 레벨 요소
    - span
    - a
    - strong
    - img
    - br
    - input
    - select
    - textarea
    - button

## inline-block 레벨 요소

- 기본적으로 inline 레벨 요소와 흡사하게 줄을 바꾸지 않고 다른 요소와 함께 한 행에 위치시킬 수 있다.
- block 레벨 요소처럼 width, height, margin, padding 프로퍼티를 모두 정의할 수 있다. 상, 하 여백을 margin과 line-height 두가지 프로퍼티 모두를 통해 제어할 수 있다.
- content의 너비만큼 가로폭을 차지한다.
- inline-block 레벨 요소 뒤에 공백(엔터, 스페이스 등)이 있는 경우, 정의하지 않은 space(4px)가 자동 지정된다.

- 프로퍼티 모음
    
    # display 프로퍼티
    
    | 프로퍼티값 키워드 | 설명 |
    | --- | --- |
    | block | block 특성을 가지는 요소(block 레벨 요소)로 지정 |
    | inline | inline 특성을 가지는 요소(inline 레벨 요소)로 지정 |
    | inline-block | inline-block 특성을 가지는 요소(inline-block 레벨 요소)로 지정 |
    | none | 해당 요소를 화면에 표시하지 않는다 (공간조차 사라진다) |
    
    ```css
    p {
      display: block;
      -webkit-margin-before: 1em;
      -webkit-margin-after: 1em;
      -webkit-margin-start: 0px;
      -webkit-margin-end: 0px;
    }
    ```
    
    - p 요소에 대한 크롬 브라우저의 디폴트 css
    
    # visibility 프로퍼티
    
    - 요소를 보이게 할 것인지 보이지 않게 할 것인지를 정의
    
    | 프로퍼티값 키워드 | 설명 |
    | --- | --- |
    | visible | 해당 요소를 보이게 한다 (기본값) |
    | hidden | 해당 요소를 보이지 않게 한다. display: none;은 해당 요소의 공간까지 사라지게 하지만 visibility: hidden;은 해당 요소의 공간은 사라지지 않고 남아있게 된다. |
    | collapse | table 요소에 사용하며 행이나 열을 보이지 않게 한다. |
    | none | table 요소의 row나 column을 보이지 않게 한다. IE, 파이어폭스에서만 동작하며 크롬에서는 hidden과 동일하게 동작한다. |
    
    # opacity 프로퍼티
    
    - 요소의 투명도 정의
    
    # background-image 프로퍼티
    
    - 요소에 배경 이미지 지정
    
    # background-repeat 프로퍼티
    
    - 배경 이미지의 반복 지정
    
    # **background-size 프로퍼티**
    
    - 배경 이미지의 사이즈 지정
    
    # **background-attachment 프로퍼티**
    
    - 화면 스크롤시 배경 이미지도 스크롤될지 결정
    
    # **background-position 프로퍼티**
    
    - 이미지의 좌표 지정
    
    # **background-color 프로퍼티**
    
    - 요소의 배경 색상 지정
    
    # **background Shorthand**
    
    - background-color, background-image, background-repeat, background-position를 한번에 정의
    
    # **font-size 프로퍼티**
    
    - 텍스트 크기 정의
    
    # **font-family 프로퍼티**
    
    - 폰트 지정
    
    # **font-style / font-weight 프로퍼티**
    
    - font-style : 이태리체 지정
    - font-weight : 폰트 굵기 지정
    
    # **font Shorthand**
    
    # **line-height 프로퍼티**
    
    - 텍스트 높이 지정
    
    # **letter-spacing 프로퍼티**
    
    - 글자 사이 간격 지정
    
    # **text-align 프로퍼티**
    
    - 텍스트 수평 정렬
    
    # **text-decoration 프로퍼티**
    
    - 링크의 밑줄 제거, 텍스트에 선 추가
    
    # **white-space 프로퍼티**
    
    - 공백, 들여쓰기, 줄바꿈 관련
    
    | 프로퍼티값 | line break | space/tab | wrapping(자동줄바꿈) |
    | --- | --- | --- | --- |
    | normal | 무시 | 1번만 반영 | O |
    | nowrap | 무시 | 1번만 반영 | X |
    | pre | 반영 | 그대로 반영 | X |
    | pre-wrap | 반영 | 그대로 반영 | O |
    | pre-line | 반영 | 1번만 반영 | O |
    
    # **text-overflow 프로퍼티**
    
    - 자동 줄바꿈이 되지 않은 텍스트 처리
    
    | 프로퍼티값 | Description |   |
    | --- | --- | --- |
    | clip | 영역을 벗어난 텍스트를 표시하지 않는다. (기본값) |   |
    | ellipsis | 영역을 벗어난 텍스트를 잘라내어 보이지 않게 하고 말줄임표(…)를 표시한다. |   |
    | <!– | <string> | 프로퍼티 값으로 지정한 임의의 문자열을 출력한다. Firefox(9.0~)만 지원하는 기능이다. –> |
    
    # **word-wrap 프로퍼티**
    
    - 한 단어의 길이가 길어서 부모 영역을 벗어난 텍스트 처리
    
    # **word-break 프로퍼티**
    
    - 한 단어의 길이가 길어서 부모 영역을 벗어난 텍스트 처리
    
    # position 프로퍼티
    
    - 요소의 위치 정의
    
    ## static (기본위치)
    
    ## relative (상대위치)
    
    ## absolute (절대위치)
    
    ## fixed (고정위치)
    
    # z-index 프로퍼티
    
    - 숫자값이 클수록 화면 전면에 출력
    
    # **overflow 프로퍼티**
    
    - 자식 요소가 부모 요소 영역을 벗어난 경우 처리
    
    | 프로퍼티값 | Description |
    | --- | --- |
    | visible | 영역을 벗어난 부분을 표시한다. (기본값) |
    | hidden | 영역을 벗어난 부분을 잘라내어 보이지 않게 한다. |
    | scroll | 영역을 벗어난 부분이 없어도 스크롤 표시한다.(현재 대부분 브라우저는 auto과 동일하게 작동한다) |
    | auto | 영역을 벗어난 부분이 있을때만 스크롤 표시한다. |
    
    # float 프로퍼티
    
    - 요소를 정렬하는데 사용
    
    | 프로퍼티값 | Description |
    | --- | --- |
    | none | 요소를 떠 있게 하지 않는다. (기본값) |
    | right | 요소를 오른쪽으로 이동시킨다 |
    | left | 요소를 왼쪽으로 이동시킨다. |
    

# 상속

- 상위 요소에 적용된 프로퍼티를 하위 요소가 물려받는 것

| property | Inherit |
| --- | --- |
| width/height | no |
| margin | no |
| padding | no |
| border | no |
| box-sizing | no |
| display | no |
| visibility | yes |
| opacity | yes |
| background | no |
| font | yes |
| color | yes |
| line-height | yes |
| text-align | yes |
| vertical-align | no |
| text-decoration | no |
| white-space | yes |
| position | no |
| top/right/bottom/left | no |
| z-index | no |
| overflow | no |
| float | no |

# 캐스캐이딩 (Cascading)

- 여러개의 CSS 적용 우선순위
    - 중요도 : CSS가 어디에 선언 되었는가
    - 명시도 : 얼마나 대상이 명확하게 특정되는가
    - 선언순서 : 선언된 순서에 따라 우선순위 적용

## 중요도

- CSS가 어디에 선언 되었는가
    1. head 요소 내의 style 요소
    2. head 요소 내의 style 요소 내의 `@import` 문
    3. `<link>` 로 연결된 CSS 파일
    4. `<link>` 로 연결된 CSS 파일 내의 `@import` 문
    5. 브라우저 디폴트 스타일시트

## 명시도

- 얼마나 대상이 명확하게 특정되었는가
    - !important > 인라인 스타일 > 아이디 선택자 > 클래스/어트리뷰트/가상 선택자 > 태그 선택자 > 전체 선택자 > 상위 요소에 의해 상속된 속성

## 선언 순서

- 나중에 선언된 스타일이 우선 적용