# HTML-CSS

# HTML

## 정의

+ Hypertext Markup Language = HTML

+ 프로그램 언어가 아니다.

+ 웹페이지가 어떻게 구조화되어 있는지 브라우저가 알 수 있도록 하는 마크업 언어.

+ elements로 구성됨.


## 요소(Element)의 기본구조

> \<p> My dog is very cute. </p\>

1. 여는 태그(Opening tag) : 요소의 이름과, 열고 닫는 꺽쇠 괄호로 구성됨, 요소가 시작부터 효과가 적용된다. 인용문에서는 앞의 \<p\>가 해당된다.

2. 닫는 태그(Closing tag) : 여는 태그와 같아보이지만 요소 앞에 슬래시(/)가 있는 것으로 단락의 끝 부분에 위치한다. 꼭 태그를 닫아주어야 한다. 그렇지 않으면 이상한 결과가 나온다. 인용문에서는 \</p\>가 해당된다.

3. 내용(Content) : 요소의 내용이며 인용문에서는 My dog is very cute. 라는 텍스트다.

4. 요소(Element) : 여는 태그, 닫는 태그, 내용을 모두 요소라고 한다.

## 포함된 요소

+ 요소 안에 다른 요소가 들어갈 수 있다. 이런 경우 포함 또는 내포되었다고 표현한다. 위의 인용문에서 very 를 강조하기 위해 \<Strong\> 이라는 요소를 중첩해서 사용할 수 있다.

> \<P> My dog is <Strong\><Strong>very</Strong>\</Strong\> cute. </p\>

## 블럭 레벨 요소, 인라인 요소

+ 블럭 레벨 요소(Block-level elements) : 블록(Block)를 만드는 요소, 블록 레벨 요소 이전과 이후에 줄 바꿈이 있다.인라인 요소에 중첩될 수 없으나 블럭 레벨 사이는 중첩될 수 있다.

+ 인라인 요소(Inline elements) : 항상 블록 레벨 요소 안에 있어야 한다. 문장, 단어 같은 작은 부분에만 적용할 수 있다. 줄 바꿈이 없다.

## 빈 요소

+ 여는 태그, 내용. 닫는 태그 패턴이 아닌, 문서에 무언가를 첨부하기 위한 단일 태그 요소.

예 : \<img\>

## 주석

+ 주석 : HTML문서에서 보이지 않으며 코드에 메모를 포함시켜 논리 또는 코딩을 설명할 수 있도록 하는 것.

> \<!-- \<p> 이것은 주석입니다.</p\> --\>

## 문서의 구조
```
<!doctype html>
<html>
    <head>
        <meta charset="utf-8"/>
        <title>My test page</title>
   </head>
   <body>
        <p>This is my page</p>
   </body>
 </html>
```
1. \<!doctype html\> : 문서 형식이 HTML5라고 선언하는 것. doctype에 따라 HTML 종류와 버전이 결정되어 그애 따라 브라우저에서 각 요소의 표현방식이나 호환되는 자바스크립트, CSS 적용방식이 달라질 수 있다.<br>문서에서 한번 만 정의되고 페이지의 가장 상단에 위치한다. 대소문자 상관없다.

2. \<html\> ~ \</html\> : HTML문서의 기본 최상단 요소로 "루트(root) 요소"라고도 부른다. 모든 다른 요소는 이 사이에 있어야 한다.

3. \<head\>~\</head\> : 주로 HTML문서에서 meta정보(이용자에게는 보이지 않지만 검색 결과에 노출될 키워드, 홈페이지 설명, CSS 스타일 등 HTML문서의 모든 내용)를 포함한다.<br> \<html\>태그와 \<body\> 태그 사이에 위치한다.<br>메타정보는 출력되지 않으며, title, charset(문자집합), style(스타일시트), script(자바스크립트), 및 기타 met정보를 정의한다. 

4. \<meta charset="UTF-8"/ \> : HTML문서의 문자 인코딩 설정을 "UTF-8"으로 지정하는 것. 지정하지 않을 경우 한글이 이상하게 출력된다.<br>문자셋(charracter set), 페이지 설명, 키워드, 저자 또는 뷰포트(viewport) 설정을 할 때 사용한다.

   + charset(문자셋)
```
<meta charset='utf-8'>
```
   + keywords(검색엔진 키워드)
```
<meta name="keywords" content="HTML, CSS, Javascript">
```

   + description(웹페이지 설명)
```
<meta name="description" content="연희 직업전문학교 웹프로그래밍 강의">
```
   + author(페이지 작성자)
```
<meta name="author" content="LEE, YONGGYO">
```
   + 새로고침 주기 설정
```
<meta http-equiv="refresh" content="30">
```
   + viewport(뷰포트)<br>장비에 따른 브라우저 화면크기에 따라 잘 보일수 있도록 설정
```
<meta name="viewport" content="width=device-width, user-scalable=yes, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
```
	- width=device-width : 웹페이지 너비를 해상도가 아닌 각 장비(device)의 브라우저 물리적 사이즈 기준으로 브라우저에 출력한다.(기기의 뷰포트 크기와 동일하게)<br>(스마트폰, 태블릿등)

	- user-scaleable : 사용자가 화면을 확대, 축소 조작을 할수 있는지 여부 yes(확대가능), no(확대불가)
	- initial-scale : 초기 로딩시 확대, 축소 여부 0~10까지 값을 가지며 1이면 기기 사이즈 기준의 원래 화면, 1보다 크면 확대 1보다 작으면(0.5, 0.3등) 축소된 화면을 출력한다. 0.5라면 50% 축소된 화면을 뜻한다.

	- maximum-scale :  확대할 수 있는 최대 범위(0~10사이 값 지정)
	- minimum-scale :  축소할 수 있는 최대 범위(0~10사이 값 지정) 

5.  <title\>~\</title\> : HTML문서의 제목을 뜻하며 텍스트로만 지정한다.<br>문서가 로드되면 브라우저 탭에 내용이 표시된다.<br>브라우저의 제목표시줄이나 페이지의 탭에 표시된다.<br>검색엔진에서 데이터 수집시 태그 사이에 지정된 내용을 바탕으로 검색페이지를 나열 하므로 검색이 잘되는 사이트를 만들때에는 꼭 title을 넣어야한다.(검색엔진 최적화 - SEO)

6. <body\>~\</body\> : HTML문서에서 실질적으로 보이는 영역을 정의하는 구간으로 텍스트, 이미지, 비디오, 게임 등 모든 콘텐츠가 포함됨.

## 속성(Attributes)

> \<p class="editor-note"> My dog is very cute. </p\>

+ 요소에 나타내고 싶지 않지만 추가적인 내용을 담고 싶을 때 사용한다. 인용문에서 class="editor-note"가 해당된다.

+ 속성을 사용할 때 지켜야하는 것.
    1. 요소 이름 다음에 오는 속성은 요소 이름과 속성 사이에 공백이 있어야 하며, 하나 이상의 속성들이 있는 경우 속성 사이에 공백이 있어야 한다. 즉 공백으로 구분해야 한다.

    2. 속성 이름 다음에는 등호(=)가 붙는다.

    3. 속성 값은 열고 닫는 따옴표(" ")로 감싸야 한다.

### HTML 속성 예시

- href  - 이동할 페이지 링크를 지정한다.
```
<a href='https://www.naver.com'>네이버</a>
```

s- rc - 이미지 경로를 지정한다.
```
<img src='photo.jpg'>
```
- width, height - 요소의 너비, 높이를 지정한다.
```
<img src='photo.jpg' width='500' height='600'>
```

- alt -이미지 대체 문구(이미지가 노출이 되지 않는 경우에 대체 노출되는 문구)
```
<img src='photo.jpg' alt='배경사진'>
```

- style - 요소에 직접 스타일을 지정한다(CSS 인라인 형태).
```
<p style='color: red;'>빨간색 글씨</p>
```
- lang - 웹페이지의 언어를 선언한다. 다만 <html>태그에만 지정한다.
```
<html lang="ko">
```
- title - 툴팁 형태로 노출되는 추가 정보를 지정할 수 있다.
```
<p title='툴팁 메세지로 노출됩니다.'>안녕하세요</p>
```


## HTML 속성 권장사항

+ 소문자로 사용
+ 속성은 소문자, 대문자 상관 없이 인식을 하나 소문자로 쓰는것을 권장한다(W3C 권장사항).
+ (title, TITLE 상관없이 인식 가능)

## HTML 헤더(Headings) 태그

### 정의

+ 헤더는 글의 제목이나 부제목을 표기할 때 사용한다.
+ 태그는 h1~h6까지 있으며, 숫자가 작을수록 크기가 크다.
> <h1>Heading 1</h1>
> <h2>Heading 2</h2>
> <h3>Heading 3</h3>
> <h4>Heading 4</h4>
> <h5>Heading 5</h5>
> <h6>Heading 6</h6>

```
<h1>Heading 1</h1>

<h2>Heading 2</h2>

<h3>Heading 3</h3>

<h4>Heading 4</h4>

<h5>Heading 5</h5>

<h6>Heading 6</h6>
```


### 주의사항
+ h1~6 태그의 용도로 헤더 태그를 사용하여야 하며 단순히 글자 크기를 크게하거나(font-size) 강조(bold)표기 용도로 사용하지 말아야 한다. 

+ 폰트 사이즈 크게 할 경우 css의 font-size 사용
+ 강조 - b 태그 또는 strong 태그 사용

## HTML 문단(Paragrahs) 태그

+ 하나의 문단을 표기 표기하는 용도로 사용하며 \<p\>~\</p\> 형태로 사용.
+ 문단을 나누는 용도로 사용하는 태그이므로 \<p\> 태그 전 후로 공백이 추가 됨.

## HTML 서식(Text Formatting) 태그

+ 텍스트 서식을 표현할수 있는 태그

   + \<b\>    굵은 텍스트 정의
   + \<em\>  강조된 텍스트 정의
   + \<i\>     기울임 꼴 텍스트 정의
   + \<small\>	더 작은 텍스트 정의
   + \<strong\> 중요한 텍스트 정의
   + \<sub\>	아래 첨자 텍스트 정의
   + \<sup\>	윗 첨자 텍스트 정의
   + \<ins\>	첨가 텍스트 정의
   + \<del\>	지운 텍스트 정의
   + \<mark\>	마킹 / 강조된 텍스트 정의

## HTML 링크(Links)

+ HTML에서 링크는 하이퍼링크다.

+ 하이퍼링크는 하이퍼텍스트 문서 안에서 직접 모든 형식의 자료를 연결하고 가리킬 수 있는 참조 고리이다. 이를테면 동영상, 음악, 그림, 프로그램, 파일, 글 등의 특정 위치를 지정할 수 있다. 이는 하이퍼텍스트의 핵심 개념이며, HTML을 비롯한 마크업 언어에서 구현하고 있다. 

+ 즉, 하이퍼텍스트 문서는 문서에 다른 문서(다른 HTML)나 이미지, 그림등의 링크를 다수 포함할 수 있고 이동할 수 있는 것을 말하여 그 링크를 하이퍼링크라고 한다.
 

### href 속성

HTML \<a\>태그는 하이퍼링크를 정의합니다. a 태그에서 가장 중요한 속성(attribute)는 href 이며 페이지를 이동할 링크(URL)을 지정할 수 있다.
```
<a href='https://www.naver.com'>네이버</a>
```

### target 속성

+ href에 지정된 링크를 통해 페이지가 변경될 경로를 지정.
+ 기본값은 \_self이며 링크가 클릭된 동일한 화면(창)에서 이동한다.

    + \_self : 기본값, 링크가 클릭된 동일한 화면.
    
    + \_blank : 링크를 클릭하면 새 창이 열리고 새창으로 페이지가 이동.

    + \_parent : iframe을 사용하고 있고 하위창에 있다면 부모창(상위 창)에서 링크를 이동.

    + \_top : iframe을 사용하고 있다면 가장 상위 창에서 링크를 이동.

## HTML 이미지(Images)

+ HTML <img>태그는 웹페이지에서 이미지를 표시하기 위해 사용.

### 필수 속성

\<img\>태그에는 2개의 필수 속성이 있다.
+ src - 이미지 경로를 지정.
+ alt - 이미지 대체 문구(이미지가 노출이 되지 않는 경우에 대체 노출되는 문구)

### width, height 속성

+ 이미지의 너비와 높이를 지정. 다만 이미지의 사이즈는 속성으로 지정하기 보다는 CSS Style로 width, height를 지정하는것이 권장됨.

### 경로

+ 절대경로
	+ 절대 경로란 특정문서 페이지 또는 이미지등 자원에 접근할 수 있는 전체 URL을 의미.
	+ photo.jpg 파일이 서버에서 /web/public/img/photo.jpg에 위치 해 있다면<br> \<a href='/web/public/img/photo.jpg'\>사진\</a\>과 같이 표현할 수 있다.

+ 상대경로
	+ 서버에서 /web/public/img/photo.jpg에 위치해 있고 현재 html 경로가 /web/public이라면 \<a href='img/photo.jpg'\> 형태로 표현할 수 있다.(현재 경로 기준)

	+ 상대경로를 표현하는 방식
	   + ./ 현재 파일이 열려 있는 경로
	   + ../ 현재 파일이 열려 있는 경로보다 1단계 상위 경로
	   + ../../ 현재 파일이 열려 있는 경로보다 2단계 상위 경로

## HTML 테이블(Tables)

+ HTML 테이블은 table, th, tr, td, thead, tbody, tfoot 등으로 구성됨. 

    + th는 테이블 헤더로 테이블 각 열을 대표하는 셀(항목)

    + tr은 데이터의 행, 가로줄

    + th는 데이터의 열, 세로줄

    + thead는 헤더영역,  tbody는 본문영역,  tfoot는 본문영역  으로 구분하여 사용할 수 있다.

<table>
<thead>
   <tr>
     <th>국어</th>
     <th>수학</th>
     <th>영어</th>
   </tr>	
</thead>
<tbody>
   <tr>
      <td>80</td>
      <td>73</td>
      <td>85</td> 
   </tr>
   <tr>
      <td>85</td>
      <td>85</td>
      <td>88</td>
   </tr>
</tbody>
</table>


```
<table>
<thead>
   <tr>
     <th>국어</th>
     <th>수학</th>
     <th>영어</th>
   </tr>	
</thead>
<tbody>
   <tr>
      <td>80</td>
      <td>73</td>
      <td>85</td> 
   </tr>
   <tr>
      <td>85</td>
      <td>85</td>
      <td>88</td>
   </tr>
</tbody>
</table>
```

## HTML 리스트(Lists)태그

### 순서 없는 리스트(Unordered HTML List)

+ 순서 없는 리스트는 \<ul\>태그로 시작하며 리스트 항목들은 \<li>~\</li\> 태그를 사용한다.

><ul>
> <li>항목1</li>
> <li>항목2</li>
> <li>항목3</li> 
</ul>


```
<ul>
<li>항목1</li>
  <li>항목2</li>
  <li>항목3</li> 
</ul>
```

+ 리스트 구분 기본 값은 disc로 색이 채워진 둥근 점 모양이다.
+ 리스트 구분 값은 css의 list-style-type으로 지정할 수 있다.
	+ disc - 기본 값, 채워진 둥근 점
	+ circle - 책이 미워진 둥근 점
	+ square - 사각형 모양 점
	+ none - 구분값 없음

- 적용방식
```
<ul style="list-style-type:disc 또는 circle, square, none 중 하나 입력">
```


### 순서 있는 리스트(Ordered HTML List)

+ 순서 있는 리스트는 \<ol\>태그로 시작하며 리스트 항목들은 \<li\>~\</li\> 태그를 사용한다.

><ol>
>  <li>항목</li>
>  <li>항목</li>
>  <li>항목</li>
></ol>

```
<ol>
  <li>항목</li>
  <li>항목</li>
  <li>항목</li>
</ol>
```

+ 리스트 구분 값은 순서가 있는 숫자나 문자로 표현이 되며 다음과 같은 타입으로 지정할 수 있다.

+ \1 - 기본값이며 숫자 순서.
+ A - 대문자 알파벳 순서.
+ a - 소문자 알파벳 순서.
+ I - 대문자 로마 숫자 형식.
+ i - 소문자 로마 숫자 형식.

   + 적용방식
```
<ol type="1 또는 A, a, I, i 중 하나 입력">
```

+ 시작번호 지정할 경우 start="시작번호"로 지정하며 숫자를 변경할 경우 \<li value="변경숫자"\>로 입력.

### 설명 리스트(Description List)

+ 용어에 대한 설명을 위한 구조로 구성되어 있는 리스트.
+ \<dl\>~\</dl\> 태그이며 하나의 행을 구성. 
+ 각 행은 \<dt\>~\</dt\>(항목명)과
+ \<dd\>~\</dd\>(항목 설명)으로 구성.

><dl>
>   <dt>상품명</dt>
>   <dd>갤럭시 S24</dd>
></dl>
><dl>
>   <dt>판매가</dt>
>   <dd>1,500,000원</dd>
></dl>

```
<dl>
   <dt>상품명</dt>
   <dd>갤럭시 S24</dd>
</dl>
<dl>
   <dt>판매가</dt>
   <dd>1,500,000원</dd>
</dl>
```

## 블럭 레벨 요소, 인라인 요소

### 블럭 레벨 요소(Block-level elements)

   + 블록(Block)를 만드는 요소, 항상 줄개행을 한다. width(너비), height(높이)를 가질 수 있다. 아래 위 또는 왼쪽 오른족에 공백(margin)을 지정할 수 있다.

   + black-level 태그(요소)
```
<address>
<article>
<aside>
<blockquote>
<canvas>
<dd>
<div>
<dl>
<dt>
<fieldset>
<figcaption>
<figure>
<footer>
<form>
<h1>
<h6>
<header>
<hr>
<li>
<main>
<nav>
<noscript>
<ol>
<p>
<pre>
<section>
<table>
<tfoot>
<ul>
<video>
```

### 인라인 요소(Inline elements)

   + 항상 블록 레벨 요소 안에 있어야 한다. 문장, 단어 같은 작은 부분에만 적용할 수 있다. 줄개행이 없다. 공간을 지정할 수 없다. 요소 안에 있는 내용 만큼의 공간만 차지한다. 위 아래 공백(margin)을 지정할 수 없으나, 내부 공백(padding)은 지정할 수 있다.

   + Inline-level 태그(요소)
```
<a>
<abbr>
<acronym>
<b>
<bdo>
<big>
<br>
<button>
<cite>
<code>
<dfn>
<em>
<i>
<img>
<input>
<kbd>
<label>
<map>
<object>
<output>
<q>
<samp>
<script>
<select>
<small>
<span>
<strong>
<sub>
<sup>
<textarea>
<time>
<tt>
<var>
```

### 인라인 블럭 요소(Inline-block Level)

   + block-level, inline-level 외에도 이 둘의 속성을 모두 가지고 있는 inline-block-level 요소.

   + 각 요소 자체에 자연적으로 있는 속성은 아니며, style 지정을 하여 적용한다.

   + block-level 속성은 style 지정을 통해 inline, inline-block level 속성으로 변경 가능. 

   + inline-level 속성은 style 지정을 통해 inline-block, block-level 속성으로 변경 가능.

   + style 적용시
   ```
   div { display: inline-block; }
   span { display: block; }
   ```

## HTML class 속성

+ class 속성은 주로 스타일시트(style sheet)에서 특정 요소(태그)를 지정할 때 사용한다. 

+ 다만 Class 속성은 동일한 이름의 class명을 지정할 수 있고 복수의 요소에 스타일을 공통적으로 지정할 수 있다.

+ 스타일시트에서 요소 선택시 점(콤마 . )으로 클래스를 지정할 수 있다.(셀렉터)

+ class='home'인 경우 ( .home ) 

+ 참고) 자바스트립트에서도 class, name tagName 등은 HTML Document Object Model(Dom)에서 복수로 선택이 되며, HTMLCollection 또는 NodeList 형태로 객체가 반환된다.

+ **주의**
+ class명은 대소문자를 구분하므로 정확하게 입력해야한다.<br>(class='home'와 class='Home'는 서로 다른 class로 인식한다.)

```
<style>
.home { 
  background-color: skyblue;
  color: white;
  padding: 20px;
  margin: 20px;
}
</style>

<div class='home'>서울</div>
<div class='home'>인천</div>
<div class='home'>부산</div>
```

## HTML id 속성

+ id 속성은 HTML 요소 중에서 유일하게 존재하는 요소에 지정한다.
+ 복수로 지정하거나 중복될 때에는 class를 사용한다.
+ 스타일시트에서 요소 선택시 샾(#)으로 id를 지정한다.(셀렉터)<br>id='page1'인 경우 #page1
+ 참고) 자바스크립트에서도 유일값으로 1개만 선택이 가능하다(document.getElementById)

```
<style>
#page1 { 
  background-color: skyblue;
  color: yellow;
}
</style>
<h1 id='page1'>페이지 제목</h1>
```

## HTML iframes

+ iframe은 웹페이지 안에서 다른 웹페이지를 보여줘야 할때 사용한다.

+ \<ifame\>~\</iframe\>태그형태로 사용

+ 속성
	+ src - iframe에 삽입될 문서의 주소
   + width, height - iframe의 너비, 높이
	+ frameborder - 테두리 표시여부(1 - 테두리 있음, 0 - 테두리 없음)
	+ scrolling - 스크롤바 유무 선택(yes - 표시, no - 없음, auto - 자동)
	+ name - target이 필요한 프레임의 이름

	   + \<iframe src='inner_iframe.html' width='1100' height='500' frameborder=0 scrolling='yes'\>\</iframe\>


## HTML Javascript 

+ HTML에서 자바스크립트를 사용해야 할 경우 \<script\>~\</script\>태그를 사용한다.
+ \<script\>태그는 브라우저에 내장된 자바스크립트 언어를 사용할때 정의한다.
+ 보통 통상적으로 \<script\>태그는 head 태그 안쪽에 넣는다. 그러나 필요에 따라서는 위치에 상관없이 추가할 수 있다.
+ HTML 문서 내부에 코드를 정의하는 방법과 자바스크립트를 외부파일에서 불러오는 방법이 있다.

### 내부에 코드를 정의하는 방법

```
<script>
window.addEventListener("DOMContentLoaded", function(e) {
    alert("HTML DOM 불러오기 완료");
}, false);

window.addEventListener("load", function(e) {
     alert("HTML 문서 호출 완료");
}, false);
</script>
```

### 외부파일에서 불러오는 방법

```
<script src='script.js'></script>
```

### 태그(요소) 속성으로 스크립트를 실행하는 방법

+ 태그의 속성명으로 자바스크립트를 실행할 수 있다. 다만 자바스크립트, 스타일시트를 HTML에 혼재하지 않고 분리하여 쓰는것이 좋으므로 꼭 필요한 경우에만 적용한다.<br>(혼재해 사용할 경우 소스가 HTML에 분산되어 있어 유지보수시에 어려움이 따른다. 따라서 따로 용도에 맞는 외부 파일로 분리하여 관리하는것이 좋다.)

```
<button onclick="alert('클릭하셨습니다.');">클릭</button>
```

### \<style\> 요소
+ HTML 페이지 안에서 스타일 정보를 정의하는데 사용한다.

### \<link\>요소
+ 현재 문서 및 외부자원 사이의 관계를 정의, 태그는 대부분 외부 스타일시트를 연결하는데 사용한다.

```
<link rel="stylesheet" type="text/css" href="style.css">
```
### \<script\>요소
+ 자바스크립트를 정의하는데 사용한다.

### \<base\>요소
- 상대경로에서 기존이 되는 URL 설정 유일한 값이므로 중복 설정할 수 없으며 \<head\>태그 최상단에 선언한다.

```
<head>
   <base href="http://test.com/test1/">
</head>
 
<a href="test2/test3.html">클릭</a>
```

+ test2/test3.html은 base에 정의한 기본 URL의 상대 경로가 되므로 http://test.com/test1/test2/test.html 의 경로도 이동하게 된다.
+ 링크뿐 아니라 내부에 선언된 외부 스타일시트, 이미지, 외부 자바크립트 경로 역시 동일하게 base값이 적용된다.

## HTML 시멘틱 요소(Semantic Elements)

+ 시멘틱 요소는 의미를 가진 요소를 뜻한다. 
+ 시멘틱 요소를 사용하면 브라우저와 개발자 모두에게 그 의미를 명확하게 설명하는 것이다.
+ 즉, 어느부분이 제목이고 어떤 부분이 내용인지, 어느부분이 메뉴인지 쉽게 파악할 수 있다.
+ 특정한 태그에 의미를 부여해서 웹페이지를 만드는것을 시멘틱웹이라 표현한다.


+ 비의미적 요소 예
	+ \<div\> 및 \<span\> : 공간을 차지하나 그 영역이나 사용용도에 대한 의미는 없다.

+ 의미적 요소 예
	- \<form\>, \<table\> \<article\> 등 : 영역, 사용용도에 대한 의미를 쉽게 알 수 있다.

### 웹페이지의 영역을 정의하는 의미 요소

+ \<header\> : 헤더영역을 정의<br>하나 이상의 제목요소(\<h1\>~\<h6\>), 로고 또는 아이콘, 저자 정보

+ \<nav\> : 탐색 링크 세트 정의<br>메인 메뉴등 GNB(Global Navigation Bar) 영역을 지정

+ \<section\> : 문서의 섹션을 정의<br>section은 공통 영역에 속하는 여러개의 article로 구성할 수 있다.
+ \<article\> : 독립적인 컨텐츠를 정의 

+ \<aside\> : 컨텐츠 이외의 컨텐츠를 정의(예 : 사이드 바)<br>서브 메뉴또는 페이지내부 메뉴를 지정. LNB(Local Navigation Bar)

+ \<footer\> : 문서 또는 섹션의 바닥 글을 정의<br>저자 정보, 저장권정보, 연락정보, 사이트 맵, 맨 위로 링크, 관련된 문서 등

+ \<details\> : 사용자가 필요에 따라 열고 닫을 수 있는 추가 세부 정보를 정의

+ \<summary\> : \<details\>요소의 제목을 정의

+ \<figure\> : 그림, 도표, 사진, 코드 목록과 같은 태그를 지정 자체에 포함 된 내용

+ \<figcaption\> : 캡션을 지정하는 figure 하위 요소

```
<figure>
   <img src="photo.jpg" alt="사진">
   <figcaption>사진 - 한국 경복궁</figcaption>
</figure>
```

+ \<main\> - 문서에서 메인영역을 명시할 경우 사용
+ \<mark\> - 문구에서 강조해야 할 부분을 정의
+ \<time\> - 날짜/시간을 정의 

+ 시멘틱 태그는 모두 div 태그와 같은 기능을 수행하는 태그다. 그러나 태그에 의미를 가지므로 검색엔진이나 그 이외의 기계적인 동작들이 웹페이지를 쉽게 이해할 수 있게 된다.


## HTML 엔티티(Entities)
+ HTML에서 일부 문자는 예약되어 있고 예약되어 있는 문자를 엔티티이름으로 사용할 수 있다.
+ 텍스트에서 작음(<) 또는 보다 큼(>)기호를 사용할때 태그로 오인될 수 있어 레이아웃 깨짐이 발생할 가능성도 있다.

   + <p> 1은 9보다 작다.(1 &lt; 9)</p>
   + <p>9는 1보다 크다.(3 &gt; 1)</p>

```
~보다 작다(<) 
<p> 1은 9보다 작다.(1 &lt; 9)</p>

~보다 크다(>)
<p>9는 1보다 크다.(3 &gt; 1)</p>
```

|Entity Name|Result|
|----|----|
|\&nbsp;|공백 1개|
|\&lt;|\<|
|\&gt;|\>|
|\&amp;|&|
|\&quot;|"|
|\&apos;|'|
|\&cent;|¢|
|\&pound;|£|
|\&yen;|¥|
|\&euro;|€|
|\&copy|©|
|\&reg;|®|


## HTML Forms
+ HTML forms은 사용자의 입력 데이터를 수집하기 위해 사용한다. 
+ 사용자가 입력한 데이터는 대부분 서버로 전송이 되며, 서버에서 처리한다.
+ \<form\>~\</form\> 태그로 구성되며 그 하위 요소에는 HTML 양식을 구성하기 위한 텍스트 필드(text), 체크박스(checkbox), 라디오 버튼(radio), 제출버튼 등으로 구성된다.

### \<input\> 요소
+ type 속성
	+ \<input\>요소는 form에서 가장 많이 사용하는 태그다.
	+ \<input\>은 type 속성에 따라서 다양하게 출력된다.
	+ \<input type="text"\> - 한줄 텍스트 입력필드를 표시한다.
	+ \<input type="password"\> - 비밀번호 입력필드를 표시한다.
	+ \<input type="radio"\> - 라디오 버튼을 표시한다(여러개 선택 항목 중 하나 선택).
	+ \<input type="checkbox"\> - 확인란을 표시한다(선택 항목을 여러개 선택).
	+ \<input type="submit"\> - 제출 버튼 표시한다.
	+ \<input type="button"\> - 클릭가능한 버튼을 표시한다.
	+ \<input type="hidden"\> - 값을 숨김 처리 하여 데이터를 전송할때 사용한다.
	+ \<input type="image"\> - 제출버튼이나 src 속성으로 이미지 제출 버튼을 만들 수 있다.

+ name 속성
	+ form 안에서 데이터 입력 필드를 추가할 때 각각의 입력필드는 name 속성 값을 지정해야 한다.
	+ name 값은 데이터를 구분하는 필드명으로 사용된다.

+ 텍스트 필드
```
<form>
   <label for="username">아이디:</label><br>
   <input type="text" name="username" id="username"><br>
   <label for="password">비밀번호:</label><br>
   <input type="password" name="password" id="password">
</form>
```

+ 라디오 버튼

```
<form>
   <input type="radio" id="male" name="gender" value="male">
   <label for="male">남자</label>
   <input type="radio" id="female" name="gender" value="female">
   <label for="female">여자</label>
</form>
```

+ 체크박스
```
<form>
  <input type="checkbox" name="vehicle[]" value="Bike" id="vehicle_bike">
  <label for="vehicle_bike">자전거</label>
  <input type="checkbox" name="vehicle[]" value="Car" id="vehicle_car">
  <label for="vehicle_car">자동차</label>
  <input type="checkbox" name="vehicle[]" value="Boat" id="vehicle_boat">
  <label for="vehicle_boat">배</label>
</form>
```

- 제출버튼
```
<form action='board_ps.php'>
   <label for="username">아이디:</label><br>
   <input type="text" name="username" id="username"><br>
   <label for="password">비밀번호:</label><br>
   <input type="password" name="password" id="password">
   <input type="submit" value="로그인">
</form>
```

### \<select\> 요소
+ 드롭다운 형태의 목록을 정의 합니다.
```
<label for="cars">자동차를 선택하세요 : </label>
<select id="cars" name="cars">
   <option value=''> - 선택하세요 -</option>
   <option value='액센트'>액센트</option>
   <option value='아반떼'>아반떼</option>
   <option value='쏘나타'>쏘나타</option>
   <option value='그랜져'>그랜져</option>
</select>
```

+ selected 속성
	+ 미리 선택된 옵션을 정의할 경우 선택 처리할 \<option\>에 selected 속성을 추가한다.
	```
	<option value='그랜져' selected>그랜져</option>
	```
	
+ size 속성
   + \<select\>에 size 속성을 지정하면 한번에 보이는 갯수를 지정할 수 있다.

```
<select id="cars" name="cars" size="3">
   <option value=''> - 선택하세요 -</option>
   <option value='액센트'>액센트</option>
   <option value='아반떼'>아반떼</option>
   <option value='소나타'>소나타</option>
   <option value='그랜져'>그랜져</option>
</select>
```

+ multiple 속성 
	+ 사용자가 둘 이상의 값을 선택할 수 있도록 할때 사용한다.

```
<select id="cars" name="cars" multiple>
   <option value=''> - 선택하세요 -</option>
   <option value='엑센트'>엑센트</option>
   <option value='아반떼'>아반떼</option>
   <option value='소나타'>소나타</option>
   <option value='그랜져'>그랜져</option>
</select>
```

### \<textarea\> 요소

+ 여러 줄을 입력할수 있는 텍스트 영역을 정의한다.
+ rows 속성 - 텍스트 영역에서 보이는 영역의 줄의 갯수를 지정한다.
+ cols 속성 - 텍스트 영역에서 보이는 폭을 지정한다.

```
<textarea name="contents" rows="10" cols="30">
내용
</textarea>
```

### Form 속성(Attributes)

+ action 속성<br>form이 제출될 때 데이터를 전송할 경로를 설정한다.
```
<form action='board_ps.php'>
   <label for="username">아이디:</label><br>
   <input type="text" name="username" id="username"><br>
   <label for="password">비밀번호:</label><br>
   <input type="password" name="password" id="password">
   <input type="submit" value="로그인">
</form>
```

+ method 속성
	+ 양식(form) 데이터를 제출할때 사용할 HTTP 전송방식을 지정한다.
	+ 일반적으로 method는 GET과 POST을 많이 사용하며, 기본값은 GET 이다(아무것도 지정하지 않은 경우).

   + GET 방식
      + URL에 변수(데이터)를 포함시켜 요청한다.
      + URL에 데이터가 노출되어 보안에 취약하다.

   + POST방식 
      + URL에 변수(데이터)를 노출하지 않고 요청한다.
      + URL에 데이터가 노출되지 않아서 기본 보안은 되어있다.


+ 자동완성(autocomplete) 속성
	+ autocomplete 속성을 켜면 브라우저는 사용자가 이전에 입력한 데이터를 기반으로 자동으로 값을 완성한다.

	+ 일반적으로 값을 지정하지 않는다면 기본으로 자동완성이 된다. 
	+ 자동완성을 사용하지 않는 경우 autocomplete='off'로 설정한다.
	
	```
	<form action='board_ps.php' autocomplete='off'>

	</form>
	```

+ enctype 속성
   + POST 방식으로 데이터를 전송할때 양식 데이터가 인코딩 되어야 할 경우 사용한다.
   + 주로 파일 업로드와 같이 file 태그와 함께 사용한다.

```
<form action='board_ps.php' method='post' enctyle="multipart/form-data">
파일 : <input type='file' name='file'>
<input type="submit" value="업로드">
</form>
```

+ target 속성
	+ form이 제출된 후 표시할 위치를 지정한다.


### HTML \<input\> 속성

+ value (초기 값)
   + 입력 필드의 초기 값을 지정한다.
```
<form action='board_ps.php'>
   <label for="username">아이디:</label><br>
   <input type="text" name="username" id="username" value='bluebird'><br>
   <label for="password">비밀번호:</label><br>
   <input type="password" name="password" id="password">
   <input type="submit" value="로그인">
</form>
```

+ readonly (읽기전용)
   + 읽기 전용 속성이며 수정이 불가 하다.
   + username은 readonly로 bluebird값으로 고정이 되며 수정이 불가해진다.
   + 그러나 개발자도구를 사용하여 값 변조는 가능하므로 반드시 데이터 처리 서버 쪽에서 데이터 검증을 해야한다.
```
<form action='board_ps.php'>
   <label for="username">아이디:</label><br>
   <input type="text" name="username" id="username" value='bluebird' readonly><br>
   <label for="password">비밀번호:</label><br>
   <input type="password" name="password" id="password">
   <input type="submit" value="로그인">
</form>
```

+ disabled (비활성화 된 속성)
   + 비활성화된 입력필드는 사용할 수 없으며 클릭 할 수 없다.
   + 비활성화된 입력필드 값은 form을 제출해도 전송되지 않는다.
```
<form action='board_ps.php'>
   <label for="username">아이디:</label><br>
   <input type="text" name="username" id="username" value='bluebird' disabled><br>
   <label for="password">비밀번호:</label><br>
   <input type="password" name="password" id="password">
   <input type="submit" value="로그인">
</form>
```

+ size (크기속성)
   + 입력 필드의 너비를 지정한다.
```
   <input type="text" name="username" id="username" size='15'>
```

+ maxlength (최대 문자 수)
   + 입력 필드에 입력 가능한 문자 수를 제한한다.
```
최대 입력 가능 문자 수를 10개로 제한 
<input type="text" name="username" id="username" maxlength='10'>
```

+ multiple (다중 속성)
   + 입력 필드에 둘 이상의 값을 입력할 수 있도록 지정한다.
   + 대표적으로 \<select\>나 \<input type='file'\>에서 사용된다.

```
<input type='file' name='files[]' multiple>
```

+ placeholder (자리표시자 속성)
   + 입력 필드의 입력 안내문구를 설정할 수 있다.
```
<input type="text" name="username" id="username" placeholder='아이디를 입력하세요.'>
```

+ required (필수속성)
   + form 제출시 반드시 입력해야 하는 필드를 정의한다.
```
username은 form 제출시 반드시 입력해야 하는 필드가 된다.
<input type="text" name="username" id="username" required>
```

+ autofocus (자동초첨 속성)
   + 페이지가 로드될 때 자동으로 focus될 필드를 설정한다.
```
<form action='board_ps.php'>
   <label for="username">아이디:</label><br>
   <input type="text" name="username" id="username" autofocus><br>
   <label for="password">비밀번호:</label><br>
   <input type="password" name="password" id="password">
   <input type="submit" value="로그인">
</form>
```

## HTML 태그 참조
- HTML 태그와 속성은 전부 암기할 수는 없다. 중요한 것은 필요할때 적절한 사용방법을 찾는 것이다.
- 어느정도 HTML 태그를 눈에 익혀 놓으면 필요할 때 쉽게 찾을 수 있다. 

- 참고 URL 
[https://github.com/yonggyo1125]


# CSS
+ CSS(Cascading Style Sheet)는 HTML과 같은 마크업 언어로 작성된 문서에 색상, 폰트, 각 요소의 위치 변경, 백그라운드 및 간단한 애니메이션(transition) 등의 효과를 주어 보다 보기 좋게 꾸며 주는 역할한다.


## HTML에서 CSS를 적용하는 방법

### HTML 요소 속성으로써 적용하는 방법
+ HTML의 각 태그에서 style 속성으로 적용. 
```
<p style="color: blue">파란색</p>
```
+ 속성으로써 적용을 하게 되면 적용의 우선 순위가 가장 높으므로 바로 적용된다. 
+ 다만 우선순위가 가장 높고, HTML의 요소 안에 분산되어 산재하므로 유지보수에 어려움이 있을 수 있다.

### CSS 적용 순서

+ 요소에서 style 속성(inline 타입)  \> #id(클래스명) \> .class(클래스명)  \> tag(태그명)

### HTML \<style\>~\</style\> 요소로 적용하는 방법

+ 같은 HTML 문서에 \<style\> 태그 안에 스타일을 적용.

```
   <!DOCTYPE html>
   <html>
     <head>
       <meta charset='UTF-8'>
       <style>
          p { color : blue; }
       </style>       
     </head>
     <body>
       <p>파란색 글씨</p>
     </body>
   </html>
```   

+ 같은 문서에 CSS가 HTML 요소로 함께 존재하게 되는 형태.

+ 여러 페이지에 공통 스타일이 있는 경우 중복해서 작성해야 하는 불편함이 있고, 중복된 소스가 분산되어 산재하므로 유지 보수에 어려움이 따를 수 있다.

### 외부 파일로 적용하는 방법(권장)

+ CSS를 외부 파일로 따로 분리하여 작성하는 방식.
```
<link rel="stylesheet" type="text/css" href='css 외부 파일 경로'>
```

``` 
<!DOCTYPE html>
   <html>
     <head>
       <meta charset='UTF-8'>
       <link rel="stylesheet" type="text/css" href="css/style/.css">
     </head>
     <body>
       <p>파란색 글씨</p>
     </body>
  </html> 
```

+ 외부파일로 따로 분리하여 작성하는 경우 공통 요소에 대한 스타일을 한 번만 정의 할 수 있다.

+ 웹브라우저는 한번 다운로드 받은 외부 파일은 캐싱처리를 하므로 브라우저의 렌더링 속도에 이점이 있다.

+ 캐싱처리를 하므로 수정한 CSS 요소가 바로 반영되지 않는 다는 문제가 있다.

## 선택자

+ 특정 요소를 선택하게 해 주는 것.

+ HTML요소에 스타일을 입힐려면 우선 특정 요소를 선택하고 선택한 요소에 스타일을 지정하여 꾸며야 한다.

### 선택자의 종류

#### 태그 선택자

+ div, span, p와 같이 태그 이름으로 요소를 선택하는 방법. 
+ 태그 이름이므로 복수의 요소를 선택할 수 있다. 

```
 <style>
p { color: red; }
 </style>
```

#### 클래스 선택자

+ 클래스 속성에 지정된 이름으로 요소를 선택하는 방법.
+ 클래스는 개념적으로 복수의 요소에 적용하기 위한 속성이므로 복수의 요소를 선택할 수 있다.
+ 클래스 선택자는 마침표(.)로 시작하며 클래스명을 입력한다.

```
<style>
.selected { color: blue }
</style>
<ul>
<li>알페온</li>
<li class='selected'>쏘나타</li>
<li>제네시스</li>
</ul>
```

#### 아이디 선택자

+ 아이디 속성으로 지정된 이름으로 요소를 선택하는 방법.
+ 아이디는 개념적으로 1개의 요소에 적용하기 위한 속성이다. 그러나 CSS에서는 여러 개가 선택될 수 있으나 적용 우선순위에 영향을 받으므로 반드시 1개의 요소만 적용하도록 한다.
+ 아이디 선택자는 샵(#)으로 시작하며 아이디명을 입력한다.

```
<style>
#title { color: red }
</style>
```

```
<h1 id='title'>제목</h1>
```

#### 스타일 적용 우선 순위(중요)
+ style 속성에 적용(inline 타입) \> #id명 \> #class명 \> tag이름
+ 스타일은 가장 많은 요소에 적용될 수 있는 범위의 선택자가 가장 우선순위가 작고, 적용 범위가 작을 수록 스타일 우선순위가 높습니다.


#### 조상 자손 선택자
+ 스타일을 적용할 요소의 범위를 좁혀서 적용하기를 원할때 사용한다. 
+ 왼쪽에 먼저 나열되는 요소가 상위 요소로 인식.

```
p 태그 아래 li 요소가 모두 선택된다.
<style>
p li { color :red; }
</style>
```

```
<p>
  <ul>
    <li>알페온</li>
    <li>쏘나타</li>
    <li>제네시스</li>
   </ul>
   <ol>
     <li>알페온</li>
     <li>쏘나타</li>
     <li>제네시스</li>
   </ol>
</p>
```

#### 부모 자식 선택자
+ 상기 예시의 경우 p 태그 아래 li로 되어 있는 모든 태그가 적용이 됩니다. 
+ ul 요소 하위 li만 적용해야 하는 경우도 있는데, 그때는 \> 결합자 를 사용하여 바로 하위 요소를 선택할 수 있다.

```
<style>
p ul > li { color: blue; } 
</style>
```

#### 그룹 선택자
+ 여러 요소를 선택하여 동일 속성을 선택하는 방법

```
<style>
ul, ol { color: red; }
.car, .truck { color: blue; }
#nav li, #footer li { font-size: 20px; }
</style>
```

#### 가상 클래스선택자

+ 선택자에 추가하는 키워드로, 선택한 요소가 특별한 상태여야 적용될 수 있는 선택자를 의미한다.

```
link -> 방문한 적이 없는 링크
visited -> 방문한 적이 있는 링크
hover -> 마우스를 롤오버 했을 때 
active -> 마우스를 클릭했을 때 
read-only -> 읽기 전용 상태일때 
not(선택자) -> 특정 포함되지 않은 요소만 선택
nth-child -> 특정 순서에 있는 요소를 선택할 때
checked -> radio, checkbox에서 선택된 요소
after -> 하위 요소 가장 끝에
before -> 하위 요소 바로 앞에
```
#### 결합자

+ 결합자니는 “A는 B의 자식”, “A는 B와 인접한 요소” 처럼 두 개 이상의 선택자 끼지 관계를 형성한다.

+ 인접 형제 결합 A + B<br>
   요소 A와 B가 같은 부모를 가지며 B가 A를 바로 뒤따라야 하도록 지정한다.
  
+ 일반 형제 결합 A ~ B<br>
   요소 A와 B가 같은 무모를 가지며, B가 A를 뒤따라야 하도록 지정한다. 그러나 B가 A의 바로 옆에 위치해야 할 필요는 없다.

+ 자식 결합자 A > B<br>
  요소 B가 A의 바로 밑에 위치해야 하도록 지정한다.

+ 자손 결합자<br>
 요소 B가 A의 밑에 위치해야 하도록 지정한다. 그러나 B가 A의 바로 아래에 있을 필요는 없다.

### 스타일 상속(inherit)
+ 스타일은 가장 효율적인 방식으로 브라우저에서 적용된다. 보통 상위 요소가 하위 요소의 스타일에 영향을 주나 모든 속성에 해당되지는 않는다.

```
color 속성은 상속된다.
border 속성은 상속되지 않는다.
``` 

## 속성

+ 스타일 각각의 효과는 속성이라고 합니다. 속성은 약 250개 정도가 있다고 하나 실제 개발 환경에서 모두 익히고 작업을 하는 경우는 거의 없다. 
+ 사용 빈도수가 낮은 경우는 바로 떠올려서 적용하기 역시 어려울 수 있다.
+ 따라서 속성에 대한 공부는 가장 많이 쓰는 속성 위주로 연습, 기억하면 된다. 

## 폰트
### font-size 
+ 글자 크기를 지정하는 속성. 주요 단위는 px, em, rem입니다.
+ rem
	+ \<html\> 태그에 적용된 font-size에 따라 상대적으로 크기가 결정됨. 
   
+ px 
	+ 모니터상의 화소 하나의 크기에 대응되는 단위. 고정된 값이기 때문에 이해하기 쉽다.
	
+ em
	+ 부모태그에 지정된 font-size에 따라 상대적으로 크기가 결정됨.

### color
+ 글꼴의 컬러를 지정할 수 있다. 
+ 색상을 지정하는 방법

   + hex 코드(16진수 코드) 적용방식 

```
 p { color: #ff0000; }
``` 
   + 색상명으로 적용하는 방식
```
 p { color: red; }
```

   + RGB 방식으로 적용하는 방식
	   + 빛의 3원색인 빨강,녹색,파랑의 수치로 적용하는 방법이며 색상의 범위는 각각 0~255(256개)씩 조합하여 색상을 구성.(16,777,216개 색상)
```
p { color: rgb(255, 0, 0); }
``` 
  
### text-align
+ 텍스트 정렬 방향을 지정할 수 있다.
	+ left : 왼쪽 정렬
	+ right : 오른쪽 정렬
	+ center : 중앙 정렬
	+ justify : 양쪽 정렬

### line-height
+ 행간 높이를 지정할 수 있다. 기본값은 1.2 다. 
   
### font-weight
+ 텍스트의 굵기를 지정할 수 있다.
+ normal(정상), bold(굵게)와 같이 텍스트로 속성을 지정하거나 100~900 범위의 숫자로 굵기를 지정할 수 있다.<br>(다만 폰트가 지원을 하는 숫자의 범위여야 적용된다.)

### font-family
+ 글꼴을 지정할 수 있는 속성. 
+ 글꼴을 지정하는 방법

```
p { font-family: 폰트명1, 폰트명2, 폰트명3 }
```
+ 폰트는 적용가능 폰트를 왼쪽부터 우선 순위를 가지고 적용된다. 
+ 즉 폰트명1이 적용되면 폰트명2는 적용되지 않는다.
+ 2개 이상 단어로 구성된 폰트명은 큰따옴표(”)로 감싸서 설정한다.

```
p { font-family : "Sans Serif", Verdana, "Times New Roman"; }
```
  
+ 폰트는 사이트를 이용하는 사용자의 컴퓨터에 자체적으로 보유하고 있는 시스템 폰트와 웹폰트로 구분한다.
+ 시스템에 설치하는 폰트는 웹 사용자에 따라 보유하고 있을 수도 있고, 없을 수도 있으므로 통일성을 위해서 또는 라이센스가 있는, 보기 좋은 폰트 사용을 위해 웹 폰트를 사용하기도 한다.

+ 웹폰트 사용하는법(중요)

```
https://fonts.google.com/


https://fonts.google.com/specimen/Noto+Sans+KR?preview.text_type=custom&selection.family=Noto+Sans+KR:wght@100;300;400;500;700;900&sidebar.open=true

<link>방식
<link rel="preconnect" href="https://fonts.gstatic.com"> <link href="https://fonts.googleapis.com/css2? family= Noto+Sans+KR:wght@100;300;400;500;700;900 & display=swap" rel="stylesheet">

import 방식
@import url('https://fonts.googleapis.com/css2? family= Noto+Sans+KR:wght@100;300;400;500;700;900 & display=swap');


font-family: 'Noto Sans KR', sans-serif
```
## 공간
### 인라인 레벨 요소(Inline level Element)
+ 줄개행을 하지 않는다.
+ 공간을 지정할 수 없다. 요소 안에 있는 내용만큼의 공간만 차지한다.
+ 위 아래 공백(margin)을 지정할 수 없으나, 내부 공백(padding)은 지정할 수 있다.
+ 대표적으로 \<span\>태그는 inline-level 요소다.

### 블록 레벨 요소(block Level Element)
+ 항상 줄개행을 한다.
+ 공간을 지정할 수 있다. 즉, width, height(너비와 높이)를 가질 수 있다.(CSS에서 지정)
+ 아래 위 또는 왼쪽 오른쪽에 공백(margin)을 지정할 수 있습니다.
+ 대표적으로 \<div\> 태그는 block-level 요소다.

### 인라인 블록 요소(Inline-Block Level Element)
+ block-level, inline-level 외에도 이 둘의 속성을 모두 가지고 있는 inline-block-level 요소도 있다.
+ 각 요소 자체에 자연적으로 있는 속성은 아니며, style 지정을 하여 적용할 수 있다.
+ block-level 속성은 style 지정을 통해 inline, inline-block level 속성으로 변경할 수 있다. 
+ inline-level 속성 역시 style 지정을 통해 inline-block, block-level 속성으로 변경할 수 있다.

### display 속성
+ display 속성을 사용하여 block, inline, inline-block, 또는 none 속성(안보임처리)를 지정하여 공간 속성을 변경할 수 있다.

```
<style>
p { display: inline; }
span { display: block; }
.section { display: none;  }
</style>
```
## 레이아웃
### box-sizing
+ box-sizing 속성을 설정하지 않는 다면 모든 요소는 기본 content-box 속성을 가진다. 

+ content-box
   + 내용이 기준이 되며, 각 요소의 기준 너비, 높이는 보더(border)와 padding이 더해진다. 
+ border-box
   + 보더가 기준이 되며, 보더 기준으로 기준 너비, 높이가 결정된다.

### 포지션
+ position 속성은 문서상의 배치하는 방법을 지정한다(top, right, bottom, left, z-index).
+ 아무 속성을 지정하지 않는다면 기본 값은 static 이다.

+ static
	+ 요소를 일반적인 문서 흐름에 따라 배치한. top, right, bottom, left, z-index 속성은 적용되지 않는다.
+ relative
	+ 요소를 일반적인 문서 흐름에 따라 배치하고 자기자신을 기준으로 top, right, bottom, left의 값에 따라 오프셋(offset)을 적용한다. 
	+ z-index에 따라 요소의 층위를 지정할 수 있다.

+ absolute
	+ 요소를 일반적인 문서 흐름에서 제거하고, 페이지 레이아웃 공간도 배정하지 않는다.
   + 대신 가장 가까운 위치 지정 조상요소에 대해 상대적으로으로 배치한다(조상 위치 기준으로 top, right, bottom, left 값 지정)단, 조상 중 위치 지정 요소가 없다면 가장 상위 블록을 기준으로 삼는다. 
	+ 조상 요소를 지정하는 방법은 상위 요소에 position: relative; 속성을 부여 하면 된다.
	+ z-index에 따라 요소의 층위를 지정할 수 있다.

+ fixed
	+ 요소를 일반적인 문서 흐름에서 제거하고 페이지 레이아웃에 공간도 배정하지 않는다.
	+ 대신 뷰포트의 초기 컨테이닝 블록을 기준으로 삼아 배치한다(즉, 브라우저에서 보이는 영역 기준으로 top, right, bottom, left 배치)

### float
	+ 왼쪽 또는 오른쪽 방향에 따라 흘러가듯이 배치
	+ left : 왼쪽 방향으로 흘러가듯이 배치
	+ right : 오른쪽 방향으로 흘러가듯이 배치 
	+ none : 초기값이며 흘러가는듯한 배치를 하지 않음

	+ float 속성은 clear를 해주지 않는다면 지정하지 않아도 다음 요소에 영향을 줄 있으므로 반드시 clear 처리한다.
```
<style>
ul.menu > li { float: left; }
ul.menu:after { clear: left; content: ''; display: block; }
</style>
<ul class='menu'>
 <li>메뉴1</li>
 <li>메뉴2</li>
 <li>메뉴3</li>
</ul>
```

### margin
+ margin 속성은 네 방향 바깥 여백 영역을 설정한다. 
+ margin-top, margin-right, margin-bottom, margin-left의 단축 속성이다.

```
/* 네 면 모두 적용 */
margin: 10px; 

/* 세로방향 | 가로 방향 */
margin: 10px 20px;

/* 위 | 가로방향 | 아래 */
margin: 10px 20px 5px;

/* 위 | 오른쪽 | 아래 | 왼쪽 */
margin: 10px 5px 15px 6px;
```

### padding
+ 요소 내부의 빈 공간을 추가합니다.
+ padding-top, padding-right, padding-bottom, padding-left의 단축 속성이다.

```
/* 네 면 모두 적용 */
padding: 10px; 

/* 세로방향 | 가로 방향 */
padding: 10px 20px;

/* 위 | 가로방향 | 아래 */
padding: 10px 20px 5px;

/* 위 | 오른쪽 | 아래 | 왼쪽 */
padding: 10px 5px 15px 6px;
```

### 다단(multi column)
+ 신문과 같이 긴 텍스트를 단을 나누어 보기 좋게 출력 할 수 있다.

+ column-count : 다단 갯수 
+ column-width : 다단별 너비
+ column-gap : 다단 사이의 여백

+ column-rule-width : 구분선 두께
+ column-rule-style : dotted(점선)|solid(직선)|thick(두꺼운 직선), 다단에 구분선을 넣는 경우
+ column-rule-color : 구분선 색상 


### media query
+ 미디어쿼리는 다양한 장비(미디에)에 따른 화면 사이즈에 적응하기 위해 특정 break-point 기준에 따라 CSS 속성을 다르게 적용하는 방법이다.

```
<style>
@media all and (max-width: 400px) {  // 화면사이즈 400px이하 적용

};
@media all and (max-width: 720px) { // 화면사이즈 720px 이하 적용
  
};

@media all and (max-width: 1024px) { // 화면사이즈 1024px 이하 적용

}
</style>
```

## 그래픽
### background
+ 배경색 또는 배경 이미지를 지정하는 속성.

### background-color 
+ 요소의 배경색상을 지정한다.
```
body { background-color: blue; }
```

### background-image 
+ 배경을 이미지로 채운다. 이미지 경로를 설정하면 좌우, 상하 반복(repeat-x, repeat-y) 속성이 기본적으로 적용되므로 요소를 가득 채운다.

```
body { background-image: url("img/photo.jpg"); }
```

### background-repeat
+ 배경이미지의 반복 속성을 지정한다.
+ no-repeat 반복 없음 
+ repeat-x : 좌우 방향으로 반복
+ repeat-y : 상하 방향으로 반복

```
body {
  background-image : url("img/photo.jpg");
  background-repeat : no-repeat;
}
```

### background-attachment
+ 배경이미지를 스크롤할지 고정할지 여부를 지정
+ fixed : 고정
+ scroll : 스크롤 

```
body {
  background-image : url("img/photo.jpg");
  background-repeat : no-repeat;
  background-attachment : scroll;
}
```

### background-position
- 배경이지미의 위치를 지정할 수 있다. 
- background-position: 좌중우(left|right|center) 상중하(top|bottom|center);
- background-position: 100px 100px; (좌측에서 100px 이동, 위에서 아래로 100px 이동)

```
body {
  background-image : url("img/photo.jpg");
  background-repeat : no-repeat;
  background-position: right top;
}
```

### background 단축형 
+ background: 색상 이미지 반복여부 스크롤여부 위치

```
body { 
  background: #ffffff url(”img/photo.jpg”) no-repeat right top;
}
```
## overflow 
+ 요소 안에 있는 컨텐츠의 크기가 영역에 비해 클 경우 통제하는 속성

+ visible : 기본속성이며, 컨텐츠 영역이 상위 영역에 비해 클 경우 영역 밖에 겹쳐지게 출력이 된다.
+ hidden : 컨텐츠 영역중 넘어서는영역을 감춤니다. 
+ scroll : 컨텐츠 영역이 넘어설 경우 스크롤바 생성
+ auto - 컨텐츠 영역이 영역을 넘어서지 않으면 아것도 발생하지 않으나 넘어설 경우 스크롤바를 생성
+ overflow-y : auto -> 상하 위치 기준으로 스크롤바 생성 
+ overflow-x : auto -> 좌우 위치 기준으로 스크롤바 생성


## transition
+ CSS 효과를 특정 지연을 주어 부드럽게 전환될 수 있도록 한다.
+ transition-delay : CSS 속성이 적용되기전 지연시간을 지정한다. 
```
transition-delay : 1s; 
```

+ transition-duration : 전환효과 진행시간
+ transition-property : CSS 속성
+ transition-property : width;  -> 가로 너비가 변할 경우 전환효과 발생
+ transition-timing-function -> 애니메이션 효과(linear, ease, ease-in, ease-out, ease-in-out)

+ transition 축약 적용
	+ transition : property(속성) duration(지연시간), timing-function(애니메이션효과), delay(전환발생전 대기시간)
```
div { 
  transition: width 2s ease-out 1s;
}
```
## flexbox(중요)
### flexbox의 기본 개념
+ 일명 flexbox라 불리는 Flexible Box module은 flexbox 인터페이스 내의 아이템 간 공간 배분과 강력한 정렬 기능을 제공하기 위한 1차원 레이아웃 모델로 설계됨. 
+ flexbox를 1차원이라 칭하는 것은, 레이아웃을 다룰 때 한 번에 하나의 차원(행이나 열)만을 다룬다는 뜻이다. 

### flexbox의 두 개의 축
+ flexbox를 다루려면 주축과 교차축이라는 두 개의 축에 대한 정의를 알아야 한다.
+ 주축은 flex-direction 속성을 사용하여 지정하며 교차축은 이에 수직인 축으로 결정된다.
+ flexbox의 동작은 결국 이 두 개의 축에 대한 문제로 환원되기 때문에 이들이 어떻게 동작하는지 처음부터 이해하는 것이 중요한다. 

#### 주축
+ 주축은 flex-direction에 의해 정의되며 4개의 값을 가질 수 있습니다.
	+ row 
	+ row-reverse 
	+ column
	+ column-reverse

+ row 혹은 row-reverse를 선택하면 주축은 인라인 방향으로 행을 따른다.

![flex1](https://github.com/yonggyo1125/curriculum300H/blob/main/2.%EC%9B%B9%ED%91%9C%EC%A4%80(48%EC%8B%9C%EA%B0%84)/2~3%EC%9D%BC%EC%B0%A8(6h)%20-%20CSS/images/flex1.png)

+ column 혹은 column-reverse 을 선택하면 주축은 페이지 상단에서 하단으로 블록 방향을 따른다. 

![flex2](https://raw.githubusercontent.com/yonggyo1125/curriculum300H/main/2.%EC%9B%B9%ED%91%9C%EC%A4%80(48%EC%8B%9C%EA%B0%84)/2~3%EC%9D%BC%EC%B0%A8(6h)%20-%20CSS/images/flex2.png)

#### 교차축
+ 교차축은 주축에 수직하므로, 만약 flex-direction(주축)이 row 나 row-reverse 라면 교차축은 열 방향을 따른다.

![flex3](https://raw.githubusercontent.com/yonggyo1125/curriculum300H/main/2.%EC%9B%B9%ED%91%9C%EC%A4%80(48%EC%8B%9C%EA%B0%84)/2~3%EC%9D%BC%EC%B0%A8(6h)%20-%20CSS/images/flex3.png)

+ 주축이 column 혹은 column-reverse 라면 교차축은 행 방향을 따른다.

![flex4](https://raw.githubusercontent.com/yonggyo1125/curriculum300H/main/2.%EC%9B%B9%ED%91%9C%EC%A4%80(48%EC%8B%9C%EA%B0%84)/2~3%EC%9D%BC%EC%B0%A8(6h)%20-%20CSS/images/flex4.png)

+ flex 요소를 정렬하고 끝을 맞추(justify)려면 어느 축이 어느 방향인지 이해하는 것이 중요하다. flexbox는 주축, 교차축을 따라 항목을 정렬하고 끝을 맞추는 각종 속성들을 적용하는 방식으로 동작한다. 

#### 시작선과 끝선
+ flexbox가 쓰기 방법(writing mode)을 가정하지 않는다는 것은 상당히 중요하다. 과거의 CSS는 왼쪽에서 오른쪽으로 향하는 가로 방향의 쓰기 방법이었다. 하지만 현대의 레이아웃은 다양한 쓰기 방법을 포괄해야 하므로, 더이상 텍스트가 문서의 왼쪽 상단에서 시작해서 오른쪽으로 향한다고 가정하지 않는다. 새 라인이 항상 아래에 쌓인다고 가정하지도 않는다.

+ flex-direction이 row고 영어 문장을 문서에 쓰고 있다면, 주축의 시작선은 왼쪽 끝, 끝선은 오른쪽 끝이 된다.

![flex5](https://raw.githubusercontent.com/yonggyo1125/curriculum300H/main/2.%EC%9B%B9%ED%91%9C%EC%A4%80(48%EC%8B%9C%EA%B0%84)/2~3%EC%9D%BC%EC%B0%A8(6h)%20-%20CSS/images/flex5.png)

+ 아랍어 문장을 쓰고 있다면, 주축의 시작선은 오른쪽 끝, 끝 선은 왼쪽 끝이 된다.

![flex6](https://raw.githubusercontent.com/yonggyo1125/curriculum300H/main/2.%EC%9B%B9%ED%91%9C%EC%A4%80(48%EC%8B%9C%EA%B0%84)/2~3%EC%9D%BC%EC%B0%A8(6h)%20-%20CSS/images/flex6.png)

+ 영어와 아랍어는 모두 가로 쓰기를 채택하고 있으므로 두 예시에서 교차축의 시작선은 flex 컨테이너의 위 끝이며 끝선은 아래 끝이다.

+ 왼쪽-오른쪽으로 생각하는 것보다 '시작선-끝선'으로 생각하는 것이 낮다.

### flex 컨테이너
+ 문서의 영역 중에서 flexbox가 놓여있는 영역을 flex 컨테이너라고 한다.
+ flex 컨테이너를 생성하려면 영역 내의 컨테이너 요소의 display 값을 flex 혹은 inline-flex로 지정해야한다.
+ 이 값이 지정된 컨테이너의 일차 자식(direct children)요소가 flex 항목이 된다.
+ display 속성만 지정하여 flex 컨테이너를 생성하면 다른 flex 관련 속성들은 아래처럼 기본 값이 지정된다.

   + 항목은 행으로 나열된. (flex-direction 속성의 기본값은 row 다).
   + 항목은 주축의 시작 선에서 시작한다.
   + 항목은 주 차원 위에서 늘어나지는 않지만 줄어들 수 있다.
   + 항목은 교차축의 크기를 채우기 위해 늘어난다.
   + flex-basis 속성은 auto로 지정된다.
   + flex-wrap 속성은 nowrap으로 지정된다.

+ 이렇게되면 flex 항목들은 각 항목 별 내부 요소의 크기로 주축을 따라 정렬된다.
+ 컨테이너의 크기보다 더 많은 항목이 있을 경우 행을 바꾸지 않고 주축 방향으로 흘러 넘치게 된다.
+ 어떤 항목이 다른 항목보다 높이 값이 크다면 나머지 모든 항목들은 그에 맞게 교차축을 따라 늘어나게 된다.

```
.box {
		display: flex;
      }
```
```
		<div class="box">
          <div>One</div>
          <div>Two</div>
          <div>Three
              <br>has
              <br>extra
              <br>text
          </div>
        </div>
```

#### flex-direction 지정
+ flex 컨테이너에 flex-direction 속성을 지정하면 flex 항목이 나열되는 방향을 변경할 수 있습니다. flex-direction: row-reverse 라고 지정하면 행으로 나열되는 것은 그대로지만 시작 선과 끝 선이 서로 바뀌게 됩니다.

+ flex-direction을 column으로 지정하면 주축이 변경되고 항목들은 열로 나열된다. 
+ column-reverse로 지정하면 그에 더해 시작 선과 끝 선이 서로 바뀌게 된다.

```
.box1 {
          display: flex;
          flex-direction: row-reverse;
        }
.box2 {
          display: flex;
          flex-direction: column-reverse;
        }
```

```
		<div class="box1">
          <div>One</div>
          <div>Two</div>
          <div>Three</div>
        </div>
      
		<div class="box2">
          <div>One</div>
          <div>Two</div>
          <div>Three</div>
        </div>
```

### flex-wrap을 이용한 복수 행 flex 컨테이너 지정
+ flexbox는 1차원 모델이지만 flex 항목이 여러 행에 나열되도록 할 수 있다. 그 경우 각 행이 새로운 flex 컨테이너라고 생각해야 한다. 공간 배분은 해당 행에서만 이루어지며 다른 행은 영향을 받지 않는다.

+ 항목이 여러 행에 나열되도록 하려면 flex-wrap 속성의 값을 wrap으로 지정한다. 
+ 항목이 하나의 행에 들어가지 않을 정도로 클 경우 다른 행에 배치된다.
+ 아래의 라이브 예시에 있는 flex 항목은 폭이 지정되어 있으며 항목들의 폭의 합은 flex 컨테이너에 들어가기에는 너무 넓다. flex-wrap 속성이 wrap으로 지정되어 있으므로 항목은 여러 행에 나열된다. 초기값과 동일한 nowrap을 지정하고 flex항목에 대한 확대/축소 방식을 별도로 지정하지 않으면 flex 항목들은 컨테이너의 폭에 맞게 줄어든다. nowrap을 지정하면 항목이 전혀 줄어들 수 없거나 충분히 줄어들 수 없을 때 흘러넘치게 된다.

```
	.box {
        display: flex;
        flex-wrap: wrap;
    }
```

```
	<div class="box">
        <div>One</div>
        <div>Two</div>
        <div>Three</div>
      </div>
```

### 축약형 속성 flex-flow 
+ flex-direction 속성과 flex-wrap 속성을 flex-flow라는 축약 속성으로 합칠 수 있다. 첫 번째 값은 flex-direction이고 두 번째 값은 flex-wrap입니다.
```
	.box {
        display: flex;
        flex-flow: row wrap;
      }
```
```
	<div class="box">
        <div>One</div>
        <div>Two</div>
        <div>Three</div>
      </div>
```

### flex 항목에 지정 가능한 속성들 

```
- flex-grow
- flex-shrink
- flex-basis
```

+ 500 픽셀의 크기를 갖는 flex 컨테이너 내에 100 픽셀 크기의 자식 세 개가 존재할 때, 사용가능한 공간 200 픽셀이 남게 된다. 기본적으로 flexbox는 이 공간을 마지막 자식 요소 다음에 빈공간으로 남겨둔다.

![flex7](https://raw.githubusercontent.com/yonggyo1125/curriculum300H/main/2.%EC%9B%B9%ED%91%9C%EC%A4%80(48%EC%8B%9C%EA%B0%84)/2~3%EC%9D%BC%EC%B0%A8(6h)%20-%20CSS/images/flex7.png)

위의 세 가지 속성을 변경한다는 것은 **flex 항목에게 사용가능한 공간**을 분배하는 방식을 변경하는 것입니다. **사용가능한 공간** 개념은 **flex 항목**을 정렬할 때 특히 중요하다.

#### flex-basis 속성 
+ flex-basis 속성은 항목의 크기를 결정한다. 이 속성의 기본값은 auto이며, 이 경우 브라우저는 항목이 크기를 갖는지 확인한다. 위의 사진 예시의 경우 항목의 크기가 100 픽셀이므로 flex-basis의 값으로 100 픽셀이 사용된다.

+ flex 항목에 크기가 지정되어 있지 않으면, flex 항목의 내용물 크기가 flex-basis 값으로 사용된다. 따라서 flex 컨테이너에서 display: flex 속성만을 지정하면 flex 항목들이 각 내용물 크기만큼 공간을 차지하게 된다.

#### flex-grow 속성
+ flex-grow 값을 양수로 지정하면 flex 항목별로 주축 방향 크기가 flex-basis 값 이상으로 늘어날 수 있게 된다. 위의 사진 예시에서 모든 항목의 flex-grow 값을 1로 지정하면 사용가능한 공간은 각 항목에게 동일하게 분배되며, 각 항목은 주축을 따라 분배받은 값만큼 사이즈를 늘려 공간을 차지한다.

+ 첫 항목의 flex-grow 값을 2로 지정하고 나머지 두 개의 항목을 1로 지정한다면 각 항목에 지정된 flex-grow 값의 비율에 따라 남은 공간이 분배된다. 각 항목의 flex-grow 비율이 2:1:1 이므로 첫 항목에게 100 픽셀, 두 번째와 세 번째 항목에게 50 픽셀씩 분배된다.

#### flex-shrink 속성
+ flex-grow 속성이 주축에서 남는 공간을 항목들에게 분배하는 방법을 결정한다면 flex-shrink 속성은 주축의 공간이 부족할때 각 항목의 사이즈를 줄이는 방법을 정의한다.
+ flex 컨테이너가 flex 항목을 모두 포함할 만큼 넉넉한 공간을 갖고 있지 않고 flex-shrink 값이 양수이면 flex 항목은 flex-basis에 지정된 크기보다 작아진다. 또한, flex-grow 속성과 마찬가지로 더 큰 flex-shrink 값을 갖는 항목의 사이즈가 더 빨리 줄어든다.

+ 항목의 최소 크기는 실제 축소량을 계산할 때 고려되기 때문에 flex-shrink 속성이 flex-grow 속성에 비해 덜 일관된 모습을 보여줄지도 모른다. 

+ ** flex-grow 와 flex-shrink 의 값이 비율임을 유의**해야한다. flex 항목의 flex 속성을 모두 1 1 200px 로 지정하고 한 항목만 크기가 늘어나는 비율을 타 항목의 두배로 하고 싶으면 해당 flex 항목의 flex 속성을 2 1 200px로 지정하면 되지만, flex 속성 값을 모두  10 1 200px로 지정하고 늘어나는 비율을 두 배로 하고 싶은 항목의 flex 속성 값만 20 1 200px로 지정해도 동일하게 동작한다. 

#### 축약형 속성 flex(중요)
+ 보통은 flex-grow, flex-shrink, flex-basis 값을 각각 사용하지 않고 이 세 속성을 한번에 지정하는 flex 축약형을 많이 사용한다. flex 축약형의 값은 flex-grow, flex-shrink, flex-basis 순서로 지정된다.

```
      .box {
        display: flex;
      }

      .one {
        flex: 1 1 auto;
      }

      .two {
        flex: 1 1 auto;
      }

      .three {
        flex: 1 1 auto;
      }
```

```
      <div class="box">
        <div class="one">One</div>
        <div class="two">Two</div>
        <div class="three">Three</div>
      </div>
```

+ flex 축약형 표현에 사용할 수 있는 미리 정의된 축약 값들이다. 이 값들 만으로도 대부분의 경우(use-case)에 대응할 수 있다.
	+ flex: initial
	+ flex: auto
	+ flex: none
	+ flex: \<positive-number\>
	
+ flex 항목을 flex: initial로 지정하면  flex: 0 1 auto 로 지정한 것과 동일하게 동작합니다. 이 경우, flex 항목들은  flex-grow가 0이므로  flex-basis값보다 커지지 않고  flex-shrink가 1이므로 flex 컨테이너 공간이 모자라면 크기가 줄어준다. 또, flex-basis가 auto이므로 flex 항목은 주축 방향으로 지정된 크기 또는 자기 내부 요소 크기 만큼 공간을 차지한다.

+ flex: auto 로 지정하면 flex: 1 1 auto로 지정한 것과 동일하며, flex:initial 과는 주축 방향 여유 공간이 있을 때 flex 항목들이 늘어나서 주축 방향 여유 공간을 채우는 점만 다릅니다.

+ flex: none으로 지정하면 flex: 0 0 auto으로 지정한 것과 동일하며 flex 컨테이너의 크기 변화에도 flex 항목 크기는 변하지 않고 flex-basis를 auto로 지정했을 때 정해지는 크기로 결정된다.  

+ 이 축약형은 더 축약해서 flex: 1 이나 flex: 2처럼 쓸 수도 있는데, 이는 flex-grow 만 지정하고 나머지는 1 0으로 사용한다는 뜻이다. 따라서 flex: 2는 flex: 2 1 0와 동일하게 처리된다.

```
	.box {
        display: flex;
      }

      .one {
        flex: 1;
      }

      .two {
        flex: 1;
      }

      .three {
        flex: 1;
      } 
```

```
      <div class="box">
        <div class="one">One</div>
        <div class="two">Two</div>
        <div class="three">Three</div>
      </div>
    
```

### 정렬, 끝 맞추기(justification), flex 항목간 여유 공간 분배 

+ flexbox의 주 기능 중 하나는 (주축과 교차축으로 표현되는) flex 컨테이너 공간 안에 flex 항목들을 정렬하고 끝 마추며 여유 공간을 항목 간에 분배하는 것. 

#### align-items
+ align-items는 flex 컨테이너에 지정하는 속성이며, 교차축을 따라 flex 항목 열을 정렬하는 방식을 지정한다. 

+ 이 속성의 (아무것도 지정하지 않았을 때 적용되는)초기 값은 stretch이며 이 값을 지정하면 flex 항목의 높이는 flex 컨테이너 내 flex 항목 행의 최대 높이로 지정된다. 따라서, flex 항목 행이 하나 일 때는 flex 항목은 교차축 방향으로 flex 컨테이너를 가득 채우게 된다.

+ 이 속성을 flex-start 로 지정하면 flex 항목의 첫 열이 교차축 방향의 시작선에 정렬된다. flex-end로 지정하면 flex 항목의 첫 열이 교차축 방향의 끝선에 정렬됩니다. center로 지정하면 flex 항목 행에 배분된 공간의 가운데 라인에 정렬된다.
	- stretch
	- flex-start
	- flex-end
	- center

```
		.box {
            display: flex;
            align-items: flex-start;
          }
```
```
        <div class="box">
          <div>One</div>
          <div>Two</div>
          <div>Three
              <br>has
              <br>extra
              <br>text
          </div>
        </div>
```

#### justify-content
+ justify-content 속성은 주축을 따라 flex 항목 행을 정렬하는 방식을 지정한다.

+ 이 속성의 (아무것도 지정하지 않았을 때 적용되는)초기 값은 flex-start이며 이 값을 지정하면 flex 항목 행 내의 항목들은 flex 컨테이너의 시작선에서 부터 정렬된다. flex-end로 지정하면 flex 항목 행의 마지막 항목이 flex 컨테이너의 끝선에서 정렬된다. center로 지정하면 flex 항목들이 flex 항목 행의 가운데 정렬된다.

+ space-between을 지정하면 주축 방향 여유 공간을 flex 항목 사이의 공간에 균등 배분합니다.

+ space-around는 시작선 및 끝선과 flex 항목간 공간도 균등 배분에 고려하므로, 시작선 및 끝선과 flex 항목 간의 공간의 크기를 1로 배분한다면 flex 항목 사이의 공간은 2로 배분한다. 

+ space-evenly로 지정하면 여유 공간을 flex 항목 사이의 공간 및 시작선 및 끝선과 flex 항목 간의 공간에 모두 균등하게 배분한다.

	+ stretch
	+ flex-start
	+ flex-end
	+ center
	+ space-around
	+ space-between
	+ space-evenly
	
```
          .box {
            display: flex;
            justify-content: flex-start;
          }
```

```
        <div class="box">
          <div>One</div>
          <div>Two</div>
          <div>Three</div>
        </div>
```

