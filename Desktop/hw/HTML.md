# HTML이란

- HyperText MarkupLanguage

# Tag

- Open tag : <==>
- Close tag : </==>

```html
<!DOCTYPE html>
<html>
<head>
    <title>Hello</title >
</head>
<body>
    <h1 style="
        color: yellow;
        background-color: red;
    ">신짱구</h1>
    <p> 안녕하세요. 저는 떡잎마을에 사는 신짱구입니다. 5살이에요.</p>

<h2>
    가족 관계
</h2>
    <p>엄마, <a href="./father.html">아빠</a>, 저, 동생. 그리고 흰둥이와 함께 살아요.</p>
</body>
</html>
```

<!DOCTYPE html> 로 시작 : HTML 5로 작성된 문서

| 태그 | 설명 |
| --- | --- |
| <html> | HTML 문서 내용 |
| <head> | head 태그 → 브라우저가 사용하는 정보 |
| <title>  | title 태그 → 문서의 제목은 Hello |
| <body> | Body 태그 → 사용자가 보는 정보 |
| <h1>  | heading 1 |
| <h2>  | heading 2 |
| <p> | paragraph |

### 제목 (Headings) 태그

- <h1> - <h6>

### 글자 형태 (Text Formatting) 태그

- 종류
    
    
    | 태그 | 설명 |
    | --- | --- |
    | <b> | bold체 |
    | <strong> | bold체와 동일, 의미론적 중요성 |
    | <i>  | Italic체 |
    | <em> | emphasized 텍스트, Italic체와 동일하나 의미론적 중요성 |
    | <small> | 작은 글씨 |
    | <mark> | 하이라이트 |
    | <del> | 취소선 |
    | <ins> | 밑줄 |
    | <sub> | 아래에 쓰인 text |
    | <sup> | 위에 쓰인 text |

### 본문 태그

- 종류
    
    
    | 태그 | 설명 |
    | --- | --- |
    | <p> | 단락 지정 |
    | <br> | 줄내림 ( 연속된 공백, 연속된 줄바꿈도 1개의 공백으로 표시 ) |
    | &nbsp | 연속 입력시 연속적 공백 삽입 |
    | <pre>  | 형식화된 text |
    | <hr> | 수평줄 삽입 |
    | <q>  | 짧은 인용문 지정 |
    | <blockquote> | 긴 인용문 블록 |

## 요소 중첩

- 요소는 중첩 가능 → 부자관계 성립

## 빈 요소

- content를 가질 수 없는 요소
- br, hr, img, input, link, meta 등

```html
<meta charset="urf-8">
```

# 어트리뷰트

- 요소의 성질, 특징을 정의하는 명세
- 요소에 추가적 정보 제공
- 시작 태그에 위치, 이름과 값의 쌍

```html
<img src="html.jpg" width="104" height="142">
```

## 글로벌 어트리뷰트

- 모든 HTML 요소가 공통으로 사용할 수 있는 어트리뷰트

## 주석

- <! —> 로 사용

## href 속성

<a href=“./father.html”>아빠</a>

- href : hyper reference의 약자
- a 태그 : 다른 페이지로 넘어가게 하는 링크 역할

### 사용 가능한 값

- 절대 URL : 웹사이트 URL
- 상대 URL : 자신의 위치를 기준으로 한 대상의 URL
- fragment identifier : 페이지 내 특정 Id를 갖는 요소의 링크

```html
<h2 id="top">Top of page!</h2>

<a href="#top">Go to top</a>
```

- 메일 : malito:(?)
- script : href=”javascript:alert(‘Hello’);”

## 디렉토리 (폴더)

작업 디렉토리 : ./

부모 디렉토리 : ../

- index.html 페이지는 생략 가능 ( 첫 시작점, 목차 개념 )

## target 속성

- 링크 클릭시 윈도우 오픈 방법
    
    
    | 속성 | 설명 |
    | --- | --- |
    | _self  | 현재 윈도우에 오픈 |
    | _blank | 새로운 윈도우나 탭에 오픈 |

# List (목록)

- <ul> : 순서없는 목록
- <ol> : 순서있는 목록
    
    
    | 속성 | 설명 |
    | --- | --- |
    | type | 순서를 나타내는 문자 지정 가능 |
    | start | 리스트 시작 번호 지정 |
    | reversed | 순서 번호 역순 지정 |

# Table (테이블)

- 표를 만들 때 사용
- <table> : 표를 감싸는 태그
    
    
    | 속성 | 설명 |
    | --- | --- |
    | border | 표 테두리 두께 지정 |
    | rowspan | 해당 셀이 점유하는 행 수 지정 |
    | colspan | 해당 셀이 점유하는 열 수 지정 |
- <tr> : 표 내부의 행
- <th> : 행 내부의 제목 셀
- <td> : 행 내부의 일반 셀


# Image (이미지)

- <img> 사용
    
    
    | 속성 | 설명 |
    | --- | --- |
    | src | 이미지 파일 경로 |
    | alt | 이미지 파일 없을 경우 표시되는 문장 |
    | width  | 이미지의 너비 |
    | height | 이미지의 높이 |

# 미디어

## audio

- <audio> 사용
    
    
    | 속성 | 설명 |
    | --- | --- |
    | src | 음악 파일 경로 |
    | preload | 재생 전에 음악 파일을 모두 불러올 것인지 지정 |
    | autoplay | 음악 파일 자동재생 개시할 것인지 지정 |
    | loop | 음악을 반복할 것인지 지정 |
    | controls | 음악 재생 도구를 표시할 것인지 지정. 재생 도구의 외관은 브라우저마다 차이가 있다. |

## video

- <video> 사용
    
    
    | 속성 | 설명 |
    | --- | --- |
    | src | 동영상 파일 경로 |
    | poster | 동영상 준비 중에 표시될 이미지 파일 경로 |
    | preload | 재생 전에 동영상 파일을 모두 불러올 것인지 지정 |
    | autoplay | 동영상 파일을 자동의 재생 개시할 것인지 지정 |
    | loop | 동영상을 반복할 것인지 지정 |
    | controls | 동영상 재생 도구를 표시할 것인지 지정. 재생 도구의 외관은 브라우저마다 차이가 있다. |
    | width | 동영상의 너비를 지정 |
    | height | 동영상의 높이를 지정 |

# form

- <form> 사용
    
    
    | 속성 | 값 | 설명 |
    | --- | --- | --- |
    | action | URL | 입력 데이터(form data)가 전송될 URL 지정 |
    | method | get / post | 입력 데이터(form data) 전달 방식 지정 |

## input

- <input> 사용
    
    
    | type 속성값 | 설명 |
    | --- | --- |
    | button | 버튼 생성 |
    | checkbox | checkbox 생성 |
    | color | 컬러 선택 생성 |
    | date | date control (년월일) 생성 |
    | datetime | date & time control (년월일시분초) 생성. HTML spec에서 drop되었다. |
    | datetime-local | 지역 date & time control (년월일시분초) 생성 |
    | email | 이메일 입력 form 생성. subumit 시 자동 검증한다. |
    | file | 파일 선택 form 생성 |
    | hidden | 감추어진 입력 form 생성 |
    | image | 이미지로 된 submit button 생성 |
    | month | 월 선택 form 생성 |
    | number | 숫자 입력 form 생성 |
    | password | password 입력 form 생성 |
    | radio | radio button 생성 |
    | range | 범위 선택 form 생성 |
    | reset | 초기화 button 생성 |
    | search | 검색어 입력 form 생성 |
    | submit | 제출 button 생성 |
    | tel | 전화번호 입력 form 생성 |
    | text | 텍스트 입력 form 생성 |
    | time | 시간 선택 form 생성 |
    | url | url 입력 form 생성 |
    | week | 주 선택 입력 form 생성 |

## select

- 여러 리스트에서 여러 아이템을 선택할 때 사용

| 태그 | 설명 |
| --- | --- |
| select | select form 생성 |
| option | option 생성 |
| optgroup | option을 그룹화한다 |

## textarea

<textarea> 사용

## button

<button> 사용

## fieldset / legend

<fieldset> : 관련 입력 양식 그룹화

<legend> : fieldset 태그 내 사용, fieldset의 제목 정의

# 공간 분할


| tag | Description |
| --- | --- |
| header | 헤더를 의미한다 |
| nav | 내비게이션을 의미한다 |
| aside | 사이드에 위치하는 공간을 의미한다 |
| section | 본문의 여러 내용(article)을 포함하는 공간을 의미한다 |
| article | 분문의 주내용이 들어가는 공간을 의미한다 |
| footer | 푸터를 의미한다 |