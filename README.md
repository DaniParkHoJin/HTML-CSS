# HTML-CSS

## HTML

### 정의

+ Hypertext Markup Language = HTML

+ 프로그램 언어가 아니다.

+ 웹페이지가 어떻게 구조화되어 있는지 브라우저가 알 수 있도록 하는 마크업 언어.

+ elements로 구성됨.


### 요소(Element)의 기본구조

> \<p> My dog is very cute. </p\>

1. 여는 태그(Opening tag) : 요소의 이름과, 열고 닫는 꺽쇠 괄호로 구성됨, 요소가 시작부터 효과가 적용된다. 인용문에서는 앞의 \<p\>가 해당된다.

2. 닫는 태그(Closing tag) : 여는 태그와 같아보이지만 요소 앞에 슬래시(/)가 있는 것으로 단락의 끝 부분에 위치한다. 꼭 태그를 닫아주어야 한다. 그렇지 않으면 이상한 결과가 나온다. 인용문에서는 \</p\>가 해당된다.

3. 내용(Content) : 요소의 내용이며 인용문에서는 My dog is very cute. 라는 텍스트다.

4. 요소(Element) : 여는 태그, 닫는 태그, 내용을 모두 요소라고 한다.

### 포함된 요소

+ 요소 안에 다른 요소가 들어갈 수 있다. 이런 경우 포함 또는 내포되었다고 표현한다. 위의 인용문에서 very 를 강조하기 위해 \<Strong\> 이라는 요소를 중첩해서 사용할 수 있다.

> \<P> My dog is <Strong\><Strong>very</Strong>\</Strong\> cute. </p\>

### 블럭 레벨 요소, 인라인 요소

+ 블럭 레벨 요소(Block-level elements) : 블록(Block)를 만드는 요소, 블록 레벨 요소 이전과 이후에 줄 바꿈이 있다.인라인 요소에 중첩될 수 없으나 블럭 레벨 사이는 중첩될 수 있다.

+ 인라인 요소(Inline elements) : 항상 블록 레벨 요소 안에 있어야 한다. 문장, 단어 같은 작은 부분에만 적용할 수 있다. 줄 바꿈이 없다.

### 빈 요소

+ 여는 태그, 내용. 닫는 태그 패턴이 아닌, 문서에 무언가를 첨부하기 위한 단일 태그 요소.

예 : \<img\>

### 주석

+ 주석 : HTML문서에서 보이지 않으며 코드에 메모를 포함시켜 논리 또는 코딩을 설명할 수 있도록 하는 것.

> \<!-- \<p> 이것은 주석입니다.</p\> --\>

### 문서의 구조
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

### 속성(Attributes)

> \<p class="editor-note"> My dog is very cute. </p\>

+ 요소에 나타내고 싶지 않지만 추가적인 내용을 담고 싶을 때 사용한다. 인용문에서 class="editor-note"가 해당된다.

+ 속성을 사용할 때 지켜야하는 것.
    1. 요소 이름 다음에 오는 속성은 요소 이름과 속성 사이에 공백이 있어야 하며, 하나 이상의 속성들이 있는 경우 속성 사이에 공백이 있어야 한다. 즉 공백으로 구분해야 한다.

    2. 속성 이름 다음에는 등호(=)가 붙는다.

    3. 속성 값은 열고 닫는 따옴표(" ")로 감싸야 한다.

#### HTML 속성 예시

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


### HTML 속성 권장사항

+ 소문자로 사용
+ 속성은 소문자, 대문자 상관 없이 인식을 하나 소문자로 쓰는것을 권장한다(W3C 권장사항).
+ (title, TITLE 상관없이 인식 가능)

### HTML 헤더(Headings) 태그

#### 정의

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


#### 주의사항
+ h1~6 태그의 용도로 헤더 태그를 사용하여야 하며 단순히 글자 크기를 크게하거나(font-size) 강조(bold)표기 용도로 사용하지 말아야 한다. 

+ 폰트 사이즈 크게 할 경우 css의 font-size 사용
+ 강조 - b 태그 또는 strong 태그 사용

### HTML 문단(Paragrahs) 태그

+ 하나의 문단을 표기 표기하는 용도로 사용하며 \<p\>~\</p\> 형태로 사용.
+ 문단을 나누는 용도로 사용하는 태그이므로 \<p\> 태그 전 후로 공백이 추가 됨.

### HTML 서식(Text Formatting) 태그

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

### HTML 링크(Links)

+ HTML에서 링크는 하이퍼링크다.

+ 하이퍼링크는 하이퍼텍스트 문서 안에서 직접 모든 형식의 자료를 연결하고 가리킬 수 있는 참조 고리이다. 이를테면 동영상, 음악, 그림, 프로그램, 파일, 글 등의 특정 위치를 지정할 수 있다. 이는 하이퍼텍스트의 핵심 개념이며, HTML을 비롯한 마크업 언어에서 구현하고 있다. 

+ 즉, 하이퍼텍스트 문서는 문서에 다른 문서(다른 HTML)나 이미지, 그림등의 링크를 다수 포함할 수 있고 이동할 수 있는 것을 말하여 그 링크를 하이퍼링크라고 한다.
 

#### href 속성

HTML \<a\>태그는 하이퍼링크를 정의합니다. a 태그에서 가장 중요한 속성(attribute)는 href 이며 페이지를 이동할 링크(URL)을 지정할 수 있다.
```
<a href='https://www.naver.com'>네이버</a>
```

#### target 속성

+ href에 지정된 링크를 통해 페이지가 변경될 경로를 지정.
+ 기본값은 \_self이며 링크가 클릭된 동일한 화면(창)에서 이동한다.

    + \_self : 기본값, 링크가 클릭된 동일한 화면.
    
    + \_blank : 링크를 클릭하면 새 창이 열리고 새창으로 페이지가 이동.

    + \_parent : iframe을 사용하고 있고 하위창에 있다면 부모창(상위 창)에서 링크를 이동.

    + \_top : iframe을 사용하고 있다면 가장 상위 창에서 링크를 이동.

### HTML 이미지(Images)

+ HTML <img>태그는 웹페이지에서 이미지를 표시하기 위해 사용.

#### 필수 속성

\<img\>태그에는 2개의 필수 속성이 있다.
+ src - 이미지 경로를 지정.
+ alt - 이미지 대체 문구(이미지가 노출이 되지 않는 경우에 대체 노출되는 문구)

#### width, height 속성

+ 이미지의 너비와 높이를 지정. 다만 이미지의 사이즈는 속성으로 지정하기 보다는 CSS Style로 width, height를 지정하는것이 권장됨.

#### 경로

+ 절대경로
	+ 절대 경로란 특정문서 페이지 또는 이미지등 자원에 접근할 수 있는 전체 URL을 의미.
	+ photo.jpg 파일이 서버에서 /web/public/img/photo.jpg에 위치 해 있다면<br> \<a href='/web/public/img/photo.jpg'\>사진\</a\>과 같이 표현할 수 있다.

+ 상대경로
	+ 서버에서 /web/public/img/photo.jpg에 위치해 있고 현재 html 경로가 /web/public이라면 \<a href='img/photo.jpg'\> 형태로 표현할 수 있다.(현재 경로 기준)

	+ 상대경로를 표현하는 방식
	   + ./ 현재 파일이 열려 있는 경로
	   + ../ 현재 파일이 열려 있는 경로보다 1단계 상위 경로
	   + ../../ 현재 파일이 열려 있는 경로보다 2단계 상위 경로

### HTML 테이블(Tables)

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

### HTML 리스트(Lists)태그

#### 순서 없는 리스트(Unordered HTML List)

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


#### 순서 있는 리스트(Ordered HTML List)

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

#### 설명 리스트(Description List)

+ 용어에 대한 설명을 위한 구조로 구성되어 있는 리스트.
+ \<dl\>~\</dl\> 태그이며 하나의 행을 구성. 
+ 각 행은 \<dt\>~</dt\>(항목명)와 \<dd\>~\</dd\>(항목 설명)으로 구성.

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

### 블럭 레벨 요소, 인라인 요소

#### 블럭 레벨 요소(Block-level elements)

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

#### 인라인 요소(Inline elements)

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

#### 인라인 블럭 요소(Inline-block Level)

   + block-level, inline-level 외에도 이 둘의 속성을 모두 가지고 있는 inline-block-level 요소.

   + 각 요소 자체에 자연적으로 있는 속성은 아니며, style 지정을 하여 적용한다.

   + block-level 속성은 style 지정을 통해 inline, inline-block level 속성으로 변경 가능. 

   + inline-level 속성은 style 지정을 통해 inline-block, block-level 속성으로 변경 가능.

   + style 적용시
   ```
   div { display: inline-block; }
   span { display: block; }
   ```

### HTML class 속성

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

### HTML id 속성

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

### HTML iframes

+ iframe은 웹페이지 안에서 다른 웹페이지를 보여줘야 할때 사용한다.

+ \<ifame\>~\</iframe\>태그형태로 사용

+ 속성
	+ src - iframe에 삽입될 문서의 주소
   + width, height - iframe의 너비, 높이
	+ frameborder - 테두리 표시여부(1 - 테두리 있음, 0 - 테두리 없음)
	+ scrolling - 스크롤바 유무 선택(yes - 표시, no - 없음, auto - 자동)
	+ name - target이 필요한 프레임의 이름

	   + \<iframe src='inner_iframe.html' width='1100' height='500' frameborder=0 scrolling='yes'\>\</iframe\>


### HTML Javascript 

+ HTML에서 자바스크립트를 사용해야 할 경우 \<script\>~\</script\>태그를 사용한다.
+ \<script\>태그는 브라우저에 내장된 자바스크립트 언어를 사용할때 정의한다.
+ 보통 통상적으로 \<script\>태그는 head 태그 안쪽에 넣는다. 그러나 필요에 따라서는 위치에 상관없이 추가할 수 있다.
+ HTML 문서 내부에 코드를 정의하는 방법과 자바스크립트를 외부파일에서 불러오는 방법이 있다.

#### 내부에 코드를 정의하는 방법

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

#### 외부파일에서 불러오는 방법

```
<script src='script.js'></script>
```

#### 태그(요소) 속성으로 스크립트를 실행하는 방법

+ 태그의 속성명으로 자바스크립트를 실행할 수 있다. 다만 자바스크립트, 스타일시트를 HTML에 혼재하지 않고 분리하여 쓰는것이 좋으므로 꼭 필요한 경우에만 적용한다.<br>(혼재해 사용할 경우 소스가 HTML에 분산되어 있어 유지보수시에 어려움이 따른다. 따라서 따로 용도에 맞는 외부 파일로 분리하여 관리하는것이 좋다.)

```
<button onclick="alert('클릭하셨습니다.');">클릭</button>
```

#### \<style\> 요소
+ HTML 페이지 안에서 스타일 정보를 정의하는데 사용한다.

#### \<link\>요소
+ 현재 문서 및 외부자원 사이의 관계를 정의, 태그는 대부분 외부 스타일시트를 연결하는데 사용한다.

```
<link rel="stylesheet" type="text/css" href="style.css">
```
#### \<script\>요소
+ 자바스크립트를 정의하는데 사용한다.

#### \<base\>요소
- 상대경로에서 기존이 되는 URL 설정 유일한 값이므로 중복 설정할 수 없으며 \<head\>태그 최상단에 선언한다.

```
<head>
   <base href="http://test.com/test1/">
</head>
 
<a href="test2/test3.html">클릭</a>
```

+ test2/test3.html은 base에 정의한 기본 URL의 상대 경로가 되므로 http://test.com/test1/test2/test.html 의 경로도 이동하게 된다.
+ 링크뿐 아니라 내부에 선언된 외부 스타일시트, 이미지, 외부 자바크립트 경로 역시 동일하게 base값이 적용된다.

### HTML 시멘틱 요소(Semantic Elements)

+ 시멘틱 요소는 의미를 가진 요소를 뜻한다. 
+ 시멘틱 요소를 사용하면 브라우저와 개발자 모두에게 그 의미를 명확하게 설명하는 것이다.
+ 즉, 어느부분이 제목이고 어떤 부분이 내용인지, 어느부분이 메뉴인지 쉽게 파악할 수 있다.
+ 특정한 태그에 의미를 부여해서 웹페이지를 만드는것을 시멘틱웹이라 표현한다.


+ 비의미적 요소 예
	+ \<div\> 및 \<span\> : 공간을 차지하나 그 영역이나 사용용도에 대한 의미는 없다.

+ 의미적 요소 예
	- \<form\>, \<table\> \<article\> 등 : 영역, 사용용도에 대한 의미를 쉽게 알 수 있다.

#### 웹페이지의 영역을 정의하는 의미 요소

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


### HTML 엔티티(Entities)
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


### HTML Forms
+ HTML forms은 사용자의 입력 데이터를 수집하기 위해 사용한다. 
+ 사용자가 입력한 데이터는 대부분 서버로 전송이 되며, 서버에서 처리한다.
+ \<form\>~\</form\> 태그로 구성되며 그 하위 요소에는 HTML 양식을 구성하기 위한 텍스트 필드(text), 체크박스(checkbox), 라디오 버튼(radio), 제출버튼 등으로 구성된다.

#### \<input\> 요소
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

#### \<select\> 요소
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

#### \<textarea\> 요소

+ 여러 줄을 입력할수 있는 텍스트 영역을 정의한다.
+ rows 속성 - 텍스트 영역에서 보이는 영역의 줄의 갯수를 지정한다.
+ cols 속성 - 텍스트 영역에서 보이는 폭을 지정한다.

```
<textarea name="contents" rows="10" cols="30">
내용
</textarea>
```

#### Form 속성(Attributes)

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


#### HTML \<input\> 속성

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

