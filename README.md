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
1. \<!doctype html\> : 문서 형식이 HTML5라고 선언하는 것. doctype에 따라 HTML 종류와 버전이 결정되어 그애 따라 브라우저에서 각 요소의 표현방식이나 호환되는 자바스크립트, CSS 적용방식이 달라질 수 있음. 문서에서 한번 만 정의되고 페이지의 가장 상단에 위치함. 대소문자 상관없음.

2. \<html\> ~ \</html\> : HTML문서의 기본 최상단 요소로 "루트(root) 요소"라고도 부른다. 모든 다른 요소는 이 사이에 있어야 한다.

3. \<head\>~\</head\> : 주로 HTML문서에서 meta정보(이용자에게는 보이지 않지만 검색 결과에 노출될 키워드, 홈페이지 설명, CSS 스타일 등 HTML문서의 모든 내용)를 포함한다.

4. \<meta charset="UTF-8"/ \> : HTML문서의 문자 인코딩 설정을 "UTF-8"으로 지정하는 것. 지정하지 않을 경우 한글이 이상하게 출력됨.

5.  \<title\>~\</title\> :HTML문서의 제목을 뜻함, 문서가 로드되면 브라우저 탭에 내용이 표시됨.

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
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>

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

- 텍스트 서식을 표현할수 있는 태그

    - \<b\>    굵은 텍스트 정의
    - \<em\>  강조된 텍스트 정의
    - \<i\>     기울임 꼴 텍스트 정의
    - \<small\>	더 작은 텍스트 정의
    - \<strong\> 중요한 텍스트 정의
    - \<sub\>	아래 첨자 텍스트 정의
    - \<sup\>	윗 첨자 텍스트 정의
    - \<ins\>	첨가 텍스트 정의
    - \<del\>	지운 텍스트 정의
    - \<mark\>	마킹 / 강조된 텍스트 정의

### HTML 링크(Links)

- HTML에서 링크는 하이퍼링크다.

- 하이퍼링크는 하이퍼텍스트 문서 안에서 직접 모든 형식의 자료를 연결하고 가리킬 수 있는 참조 고리이다. 이를테면 동영상, 음악, 그림, 프로그램, 파일, 글 등의 특정 위치를 지정할 수 있다. 이는 하이퍼텍스트의 핵심 개념이며, HTML을 비롯한 마크업 언어에서 구현하고 있다. 

- 즉, 하이퍼텍스트 문서는 문서에 다른 문서(다른 HTML)나 이미지, 그림등의 링크를 다수 포함할 수 있고 이동할 수 있는 것을 말하여 그 링크를 하이퍼링크라고 한다.
 

#### href 속성

HTML \<a\>태그는 하이퍼링크를 정의합니다. a 태그에서 가장 중요한 속성(attribute)는 href 이며 페이지를 이동할 링크(URL)을 지정할 수 있다.
```
<a href='https://www.naver.com'>네이버</a>
```

#### target 속성

- href에 지정된 링크를 통해 페이지가 변경될 경로를 지정.
- 기본값은 \_self이며 링크가 클릭된 동일한 화면(창)에서 이동한다.

    + \_self : 기본값, 링크가 클릭된 동일한 화면.
    
    + \_blank : 링크를 클릭하면 새 창이 열리고 새창으로 페이지가 이동.

    + \_parent : iframe을 사용하고 있고 하위창에 있다면 부모창(상위 창)에서 링크를 이동.

    + \_top : iframe을 사용하고 있다면 가장 상위 창에서 링크를 이동.

### HTML 이미지(Images)

- HTML <img>태그는 웹페이지에서 이미지를 표시하기 위해 사용.

#### 필수 속성

\<img\>태그에는 2개의 필수 속성이 있다.
- src - 이미지 경로를 지정.
- alt - 이미지 대체 문구(이미지가 노출이 되지 않는 경우에 대체 노출되는 문구)

#### width, height 속성

- 이미지의 너비와 높이를 지정. 다만 이미지의 사이즈는 속성으로 지정하기 보다는 CSS Style로 width, height를 지정하는것이 권장됨.

#### 경로

- 절대경로
	- 절대 경로란 특정문서 페이지 또는 이미지등 자원에 접근할 수 있는 전체 URL을 의미.
	- photo.jpg 파일이 서버에서 /web/public/img/photo.jpg에 위치 해 있다면 \<a href='/web/public/img/photo.jpg'\>사진\</a\>과 같이 표현할 수 있다.

- 상대경로
	- 서버에서 /web/public/img/photo.jpg에 위치해 있고 현재 html 경로가 /web/public이라면 \<a href='img/photo.jpg'\> 형태로 표현할 수 있다.(현재 경로 기준)

	- 상대경로를 표현하는 방식
	    - ./ 현재 파일이 열려 있는 경로
	    - ../ 현재 파일이 열려 있는 경로보다 1단계 상위 경로
	    - ../../ 현재 파일이 열려 있는 경로보다 2단계 상위 경로

### HTML 테이블(Tables)

- HTML 테이블은 table, th, tr, td, thead, tbody, tfoot 등으로 구성됨. 

    - th는 테이블 헤더로 테이블 각 열을 대표하는 셀(항목)

    - tr은 데이터의 행, 가로줄

    - th는 데이터의 열, 세로줄

    - thead는 헤더영역,  tbody는 본문영역,  tfoot는 본문영역  으로 구분하여 사용할 수 있다.

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

- 순서 없는 리스트는 <ul>태그로 시작하며 리스트 항목들은 <li>~</li> 태그를 사용한다.

```
<ul>
<li>항목1</li>
  <li>항목2</li>
  <li>항목3</li> 
</ul>
```

- 리스트 구분 기본 값은 disc로 색이 채워진 둥근 점 모양이다.
- 리스트 구분 값은 css의 list-style-type으로 지정할 수 있다.
	- disc - 기본 값, 채워진 둥근 점
	- circle - 책이 미워진 둥근 점
	- square - 사각형 모양 점
	- none - 구분값 없음

- 적용방식
```
<ul style="list-style-type:disc 또는 circle, square, none 중 하나 입력">
```


#### 순서 있는 리스트(Ordered HTML List)

- 순서 있는 리스트는 \<ol\>태그로 시작하며 리스트 항목들은 \<li\>~\</li\> 태그를 사용한다.

```
<ol>
  <li>항목</li>
  <li>항목</li>
  <li>항목</li>
</ol>
```

- 리스트 구분 값은 순서가 있는 숫자나 문자로 표현이 되며 다음과 같은 타입으로 지정할 수 있다.

- \1 - 기본값이며 숫자 순서.
- A - 대문자 알파벳 순서.
- a - 소문자 알파벳 순서.
- I - 대문자 로마 숫자 형식.
- i - 소문자 로마 숫자 형식.

   - 적용방식
```
<ol type="1 또는 A, a, I, i 중 하나 입력">
```

- 시작번호 지정할 경우 start="시작번호"로 지정하며 숫자를 변경할 경우 \<li value="변경숫자"\>로 입력.

#### 설명 리스트(Description List)

- 용어에 대한 설명을 위한 구조로 구성되어 있는 리스트.
- \<dl\>~\</dl\> 태그이며 하나의 행을 구성. 
- 각 행은 \<dt\>~\</dt\>(항목명)와 \<dd\>~\</dd\>(항목 설명)으로 구성.

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