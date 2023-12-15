# HTML-CSS

## HTML

### 정의

Hypertext Markup Language = HTML
프로그램 언어가 아니다.

웹페이지가 어떻게 구조화되어 있는지 브라우저가 알 수 있도록 하는 마크업 언어.

elements로 구성됨.


### 요소(Element)의 기본구조

> \<P> My dog is very cute. </p\>

1. 여는 태그(Opening tag) : 요소의 이름과, 열고 닫는 꺽쇠 괄호로 구성됨, 요소가 시작부터 효과가 적용된다. 인용문에서는 앞의 \<P\>가 해당된다.

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

+ 여는 태그, 내용. 닫는 태그 패턴이 아닌, 문서에 무언가를 첨부하기 위한 단일 태그 요소.예 : \<img\>

