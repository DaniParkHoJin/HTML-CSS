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

> \<!doctype html\><br>
> \<html\><br>
>  \<head\><br>
>    \<meta charset="utf-8"/ \><br>
>    \<title>My test page</title\><br>
>   \</head\><br>
>   \<body\><br>
>    \<p>This is my page</p\><br>
>   \</body\><br>
> \</html\>

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


