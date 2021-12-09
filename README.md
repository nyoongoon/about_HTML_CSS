# about_HTML_CSS
HTML과 CSS를 공부하며 알게 된 것들을 기록하는 저장소입니다.


# 태그 vs 엘리먼트
- 태그-> 시작태그(\<a\>), 종료태그(\</a\>), 빈태드 (\<br/\>)
- 시작태그는 속성과 값을 가질 수 있음.
- 엘리먼트 : 내용을 포함해 시작태그와 종료태그 까지. 
HTML \<area\> 태그 
<br/><br/>
# tags 
<br/><br/>
### \<label\>
- 라벨 요소는 for 속성을 사용하여 다른요소와 결합 가능. for의 값은 다른 요소의 id 값. 라벨을 결합하고자 하는 요소 내부에 위치시키면 for사용 안해도 결합 가능.
- 브라우저에 의해 일반적인 텍스트로 렌더링되지만, 마우스로 클릭할 경우 라벨과 연결된 요소를 곧바로 선택할 수 있음.
- 라벨을 요소로 사용할 수 있는 요소들
: \<button\>, \<input\>, \<meter\>, \<output\>, \<progress\>, \<select\>, \<textarea\>
<br/><br/>
### \<select\>
- name 속성 : 드롭다운 리스트의 이름을 명시. + 폼(form)이 제출된 후 서버에 폼 데이터를 참조하기 위해 사용되거나, 자바스크립트에서 요소를 참조하기 위해 사용됨.
<br/><br/>
### \<option\>
- value 속성 : 폼을 제풀할 때 서버로 보내지는 값. value속성이 명시되지 않으면 해당 값은 옵션 요소 내의 텍스트로 자동 설정됨.
<br/><br/>




# \<map\> 태그
- 클라이언트 사이드 이미지맵을 정의할 때 사용. 
- 이미지맵은 클릭할 수 있는 영역을 가지는 이미지를 의미.
- \<area\> 요소는 이러한 이미지맵의 클릭할 수 있는 영역을 정의하는데 사용, \<map\>요소는 하나 이상의 \<area\>요소를 포함.
- \<map\> 요소의 필수 속성인 name속성은 \<img\> 요소의 usemap 속성과 결합, 이미지와 맵사이의 관계를 설정. 
<br/><br/>
### shape 속성 
- 영역(area)의 모양을 명시. 
- shape 속성은 해당 영역의 크기와 모양, 배치 등을 명시하기 위해 coords속성과 함께 사용.
- \<area shape="default|rect|circle|poly"\>
<br/><br/>
### coords 속성
- coords은 이미지맵에서 해당\<area\>요소의 좌표를 명시. 
- 해당 영역의 왼쪽 위 모서리의 좌표는 (0,0)
- 속성값
: x1, y1, x2, y2
: x, y, 반지름
: x1, y1, x2, y2 ,,, xn, yn(첫번째와 마지막이 일치하지 않으면, 브라우저가 자동으로 마지막 좌표쌍을 추가함)
<br/><br/>

# \<a\> 태그
- target 속성
- 속성값.
: blank 링크된 문서를 새로운 윈도우나 탭에서 오픈함. 
<br/><br/>
# \<form\>태그
- target 속성
: 폼 데이터를 서버로 제출한 후 받는 응답이 열릴 위치를 명시. 
<br/><br/>

# \<dl\> -> dictionnary list 
## \<dd\>, \<dt\>
<br/><br/>
# img 태그
- alt 속성
: 이미지 파일이 없을 경우 대체할 문자열
<br/><br/>
# fieldset 요소
- 웹 양식의 여러 컨트롤과 레이블(\<label\>)을 묶을 때 사용.
- HTML양식 속에서 그룹을 만드며 \<legend\>요소로 그룹의 설명을 제공할 수 있다. 
### attribute
- diable : 모든 자손컨트롤을 비활성화
- form : fieldset이 form안에 있지 않아도 form의 id로 요소를 연결해줌.
- name : 그룹과 연관지을 이름. 
<br/><br/>

# Display && Position 

## position
- 요소에 CSS 속성으로 position을 지정하여 속성의 상대적, 절대적 위치를 지정할 수 있다.
## position의 속성
- position : html 요소의 위치를 결정하는 방식을 설정.
- top : 위치가 설정된 조상 요소의 위로부터의 여백을 설정.
- right : 위치가 설정된 조상 요소의 오른쪽으로부터의 여백을 설정.
- bottom : 위치가 설정된 조상 요소의 아래로부터의 여백을 설정.
- left : 위치가 설정된 조상 요소의 왼쪽으로부터의 여백을 설정.
- z-index : 겹처지는 요소들이 쌓이는 스택의 순서를 설정.
- clip : 절대 위치 지정방식으로 위치한 요소를 자름.
- curosr : 표시되는 마우스 커서의 모양을 설정. 


## position 속성
### position: static
- top, right, bottom, left 속성값에 영향을 받지 않음.
- 단순히 웹페이지의 흐름에 따라 차례대로 요소들을 위치.
- 기본값. 부모 요소를 기준으로 한 위치로써, 자식 엘리먼트의 크기에 따라서 부모 엘리먼트의 크기가 자동으로 변경됨. left, top, right, bottom과 같은 offset은 무시됨.
### position: relative
- 해당 html 요소의 기본 위치를 기준으로 위치를 설정.
- html요소의 기본 위치란 해당 요소가 정적 위치 지정 방식일 때 결정되는 위치.
- 자기 자신의 위치를 기준으로 한 상대적인 위치로서, top, left, right, bottom 등의 속성값을 지정해 기준 위치로부터 얼마나 떨어진 지점에 해당 요소를 배치할 것인지 지정. 자식 엘리먼트의 크기에 따라서 부모 엘리먼트의 크기가 자동으로 변경되지만, 엘리먼트의 위치에 따라서는 변경되진 않음. 
### position: absolute
- absolute 방식은 해당 요소의 바로 상위의 위치가 설정된 조상 요소에 따라 위치를 재조정하는 방식. 
- cf) 위치가 설정된 요소라는 것은 정적 위치 지정 방식을 제외한 다른 방식으로 위치가 설정된 요소를 의미. 
- absolute 방식은 fixed 방식이 뷰포트를 기준으로 위치를 결정하는 것과 비슷하게 동작. 
- 단지 뷰포트를 기준으로 하는 것이 아닌 **위치가 설정된 조상 요소(relative)를 기준**으로 위치를 설정. 
- 위치가 설정된 **조상요소를 가지지 않는다면 html 문서의 body요소를 기준**으로 위치를 설정. 
- 부모 요소의 위치를 기준으로 한 상대 위치를 지정. **부모 요소는 relative**이어야 하며 요소의 크기가 부모 요소의 크기에 반영되지 않으므로 주의. 
### position: fixed
- 뷰포트를 기준으로 위치를 설정.
- 웹페이지가 스크롤 되어도 고저우이치로 지정된 요소는 항상 같은 곳에 위치. 
- 브라우저 창을 기준으로 위치를 지정. 전체 문서를 기준으로 위치가 정해지므로 부모 엘리먼트의 위치와는 무관하며 요소의 크기가 부모 요소의 크기에 반영되지는 않음. 또한 스크롤의 영향을 받지 않고 위치가 고정되므로 주로 특정 UI요소를 브라우저 화면에 고정할 때 사용하게 됨. 
<br/>

## display
- 각각의 요소는 특성에 따라 block 혹은 inline 속성을 가지고 있음. 
- block : 언제나 새로운 라인에서 시작. 해당 라인의 모든 너비를 차지. div, h1, p, ul, ol, form
- inline : 새로운 라인에서 시작x. 요소의 너비는 해당 html요소 만큼만 차지. span, a, img
- cf) display 속성값을 인라인에서 블록으로 변경했더라도, 변경된 요소는 내부에 다른 요소를 포함할 수 없다. 처음부터 display 속성값이 블록인 요소만이 내부에 다른 요소를 포함할 수 있기 때문. 
- inline-block : 해당 요소 자체는 inline요소 처럼 동작. 요소 내부에서는 block처럼 너비와 높이, 여백을 설정할 수 있음.
- none
- flex
- grid
## display: flex
- FlexBox는 UI레이아웃 디자인에 최적화된 모듈. display 속성의 값을 flex로 지정하게 되면 flexbox속성을 사용할 수 있음. 
- 요소의 크기가 불분명하거나 동적인 경우에도, 각 요소를 정렬할 수 있는 효율적인 방법을 제공. 
- Container는 Items를 감싸는 부모요소. 각 Item을 정렬하기 위해선 Container가 필수.
## container 용 속성
### display 
- flex Container를 정의
- display: flex -> Block 특성(수직 쌓임)의 Flex Container를 정의
- display: inline-flex -> Inline 특성(수평 쌓임)의 Flex Container를 정의
- 여기서 말하는 수직과 수평 쌓임은 Items가 아니라 **Container**라는 것에 주의. 두 값의 차이는 내부의 Items에는 영향을 주지 않는다. 
### flex-flow (주축  여777러줄묶음)
- 이 속성은 단축 속성으로 Flex Items의 주 축(main-axis)을 설정하고 Items의 여러 줄 묶음(줄 바꿈)도 설정함.
- flex-flox: 주축 여러줄묶음;
- 사용 예) flex-flow: flex-direction값 flex-wrap값;

### flex-direction : (주 축)
- Items의 주 축(main-axix)을 설정.
- item 블럭이 쌓이는 방향을 지정.
- row (기본값) : Items를 수평축(왼-오)으로 표시
- row-reverse : Items를 row 반대 축으로
- column : Items를 수직축으로 표시
- column-reverse : Items를 column의 반대 축으로 표시

### 주 축(main-axis)과 교차 축(cross-axis)
- flex-direction 에서 언급했던 주 축과 교차축의 개념.
- 값 row는 수평축을 의미하므로 이 떄의 주축은 수평, 교차축은 수직.
- column은 주축은 수직, 교차축은 수평.
### 시작점(flex-start)와 끝점(flex-end)
- 설정된 주축에 따라 시작점과 끝점이 달라짐.


### flex-wrap : (여러 줄 묶음)
- Items의 여러 줄 묶음(줄 바꿈)을 설정
- 아이템들의 크기가 container 크기를 넘어설 경우 크기를 줄일지 말지를 결정.
- nowrap(기본값) : 모든 Items를 여러 줄로 묶지 않음(한 줄에 표시)
- wrap : Items를 여러 줄로 묶음
- wrap-reverse : Items를 wrap의 역 방향으로 여러 줄 묶음.

### justify-content : (정렬방법)
- 주 축의 정렬 방법을 설정.
- 각각의 item들이 row 방향으로 차지하는 공간을 지정.
- flex-start : Items를 시작점으로 정렬
- flex-end : Items를 끝점으로 정렬
- center: Items를 가운데 정렬
- space-between : 시작 Item은 시작점에, 마지막 Item은 끝점에 정렬되고 나머지 Item은 사이에 고르게 정렬 됨. 
- space-around : Items를 균등한 여백을 포함하여 정렬

### align-content : (정렬방법)
- 교차축의 정렬방법을 설정.
- flex-wrap 속성을 통해 Items가 여러 줄이고 여백이 있을 경우만 사용. (Itmes가 한 줄일 경우 align-items 속성을 사용)
- 각각의 아이템들 정렬하기. 
- stretch : Container의 교차 축을 채우기 위해 Items을 늘림. 
- cf) stretch는 교차 축에 해당하는 너비(width 혹은 height)가 값이 auto일 경우 교차 축을 채우기 위해 자동으로 늘어남.
- flex-start : Items를 시작점으로 정렬
- flex-end : Items를 끝점으로 정렬
- center : Items 가운데를 정렬
- space-between : 시작 Item은 시작점에, 마지막 Item은 끝점에 정렬되고 나머지 Items는 사이에 고르게 정렬됨
- space-around : Items를 균등한 여백을 포함하여 정렬.

### align-items : (정렬방법)
- 교차 축에서 Items의 정렬 방법을 설정
- Items가 한 줄일 경우 많이 사용.
- Items가 flex-wrap을 통해 여러 줄 일 경우에는 align-content 속성이 우선. 따라서 align-items를 사용하려면 align-content 속성을 기본값으로 설정.
- 각각의 item들이 column 방향으로 차지하는 공간을 지정.
- stretch(기본값) : Container의 교차 축을 채우기 위해 Items를 늘림
- flex-start: Items를 각 줄의 시작점(flex-start)으로 정렬
- flex-end: Items를 각 줄의 끝점(flex-end)으로 정렬
- center: Items를 가운데 정렬
- baseline: Items를 문자 기준선에 정렬


## item 용 속성
- order : Flex Item의 순서를 설정
- flex : flex-grow, flex-shrink, flex-basis의 단축 속성
- flex-grow: Flex Item의 증가 너비 비율을 설정
- flex-shrink: Flex Item의 감소 너비 비율을 설정
- flex-basis: Flex Item의 (공간 배분 전) 기본 너비 설정
- align-self: 교차 축에서 Item의 정렬 방법을 설정

### order
- 아이템 중 우선할 항목을 숫자로 지정. 기본값은 0부터 순차적으로 겨져 있다. 
### flex: grow shrink basis
### flex-grow 
- 아이템이 차지하는 공간의 비율을 지정. 0부터 숫자가 클수록 공간을 많이 차지.
### flex-shrink
- 아이템이 차지하는 공간의 비율을 지정. 0부터 숫자가 클수록 공간을 적게 차지.
### flex-basis
- 아이템이 차지하는 크기 고정. flex방향에 따라 너비/높이가 지정됨.
### align-self 
- 개별 아이템의 align을 지정.
<br/>

## float
- float은 이전에 많이 사용하던 방식. 
- float 되지 않는 요소는 clear: both속성을 이용해 float 해지해야함.
<br/><br/>

# pseudo element 가상요소 (::before, ::after의 정의)
### 가상 클래스
- 가장클래스는 별도의 클래스를 지정하지 않아도 지정한 것처럼 요소를 선택할 수 있다. 
### 가상 요소
- 가장 클래스처럼 선택자에 추가되며, 존재하지 않은 요소를 존재하는 것처럼 부여하여 문서의 특정 부분을 선택 가능하게 한다. 
- ex)
- ::first-line -> 요소의 텍스트에서 첫 줄에 스타일을 적용.
- ::first-letter -> 요소의 첫 번째 글자에 스타일을 적용.
- ::before -> 요소의 콘텐츠 시작부분에 생선성된 콘텐츠를 추가. (실제 내용 바로 앞에서 생성되는 자식요소)
- ::after -> 요소의 콘텐츠 끝부분에 생성된 콘텐츠를 추가. (실제 내용 바로 뒤에서 생성되는 자식요소)
- ::selection -> 요소의 텍스트에서 사용자에 의하여 선택된 영역의 속성을 변경.
- ::placeholder -> input 필드에 힌트 텍스트에 스타일을 적용.
### content=""
- ::before와 ::after와 함께 쓰이는 content는 가짜 속성.
- HTML문서에 정보로 포함되지 않은 요소를 CSS에서 새롭게 생성시켜줌.
<br/><br/>

# Height
## scrollHeight vs offsetHeight vs clientHeight 
- 세 속성 모두 정수값으로 표현되며, 마진값은 공통적으로 제외. 
### scrollHeight
- 요소에 들어 있는 컨텐츠의 전체 높이. 패딩과 테두리가 포함되고 마진은 제외.
### offsetHeight
- 요소의 높이. 패딩, 스크롤 바, 테두리가 포함되고 마진은 제외.
- CSS로 요소의 높이를 지정할 때 정해지는 높이.
- box-sizing 모델 속성 값에 따라 패딩과 테두리 값이 제외될 수 있으므로 주의.
- 요소가 감춤 상태인 경우 0을 반환.
### clientHeight
- 요소의 내부 높이. 패딩 값은 포함되며 스크롤바, 테두리, 마진 제외.
<br/><br/>

# IMG의 srcset과 siezs 속성

### srcset 속성
- 1. 이미지 소스의 세트
- **같은 비율**의 다양한 크기를 가지는 동일 이미지들을 최소 2개 이상 명시하는 속성. 
- 만약 1개의 이미지 소스만 명시하려먼 src 속성을 사용함.
- 2. **브라우저에 이미지 선택권을 위임하는 속성.** 
- 3. cf) 다른 비율의 다양한 크기의 다른 이미지들을 사용하고 싶다면, CSS의 @media 사용을 권장. 
- 4. x와 w 디스크립터는 개발자가 브라우저에 이미지의 크기를 알려주는 용도의 단위.
- 브라우저가 비용 지불 없이도 이미지의 크기를 알 수 있도록 개발자가 x 혹은 w 디스크립터로 이미지 크기를 명시. 


### 예시
``` 
<img
  srcset="images/heropy_small.png 400w,
          images/heropy_medium.png 700w,
          images/heropy_large.png 1000w"     
  sizes="(max-width: 500px) 444px,
         (max-width: 800px) 777px,
         1222px"
  src="images/heropy.png"
  alt="HEROPY" />
```
- srcset 속성은 쉼표로 구분된 사용할 이미지들의 경로와 해당 이미지의 원본 크기를 지정.
- sizes 속성은 쉼표로 구분된 미디어조건과 그에 따라 최적화되어 출력할 이미지 크기를 지정. 


<br/><br/><br/><br/>

# 노마드 클론코딩 1강 (HTML) 
### HTML vs CSS
- HTML 
: 브라우저에게 콘텐츠가 무엇인지 알려줌
: markup language (markup == content)

- CSS
: 브라우저에게 콘텐츠가 어떻게 보여야하는지 알려줌
 

- Javascript 
: 다이나믹 인터랙티브

### 폴더명, 파일명 항상 소문자로 작성.

## HTML Tag
ex)
```
<h1></h1>
```

### 리스트
-ol(순서o)
-ul(순서x)
-li(list item)

### a tag (anchor)
```
<a href="~"></a>
```
- a=태그
- href=속성
- target 속성 
: target="_self" (기본값) ->현재창에서 이동
: target="_blank" -> 새창에서 이동

### img tag (이미지 태그)
```
<img/> -> 자체 닫기 태그(self closing tag)
```
: src 속성 -> 이미지의 위치 (확장자 정확하게 적기)


# HTML문서의 시작
```
<!DOCTYPE html>
<html>
	<head>

	</head> //웹사이트의 환경설정 -> 브라우저에서 보이지 않음
	<body>

	</body>	//사용자가 볼 콘텐츠
</html>
```
### \<html\>
- html문서임을 알려줌
- 속성
: lang="en" -> 검색엔진들에게 도움을 줌

### \<head\>
- 웹사이트의 환경설정 -> 브라우저에서 보이지 않음
- \<title\>
- \<meta\> 
: 부가정보. 속성 -> content, name, charset, property..
```
<meta property="og:title,type,image,description..." --> (open graph)
```
- \<link\> -> 타이틀에 이미지 삽입.
: rel="shortcut icon"(relationship),sizes="", href="~"


# Form tags
### \<input\>
-  속성들
: type -> 기본값은 text. ...
: type = "file" -> accept로 파일 종류 제한 가능  
: placeholder -> 인풋 미리 채워줌 
: required -> 반드시 채워야 함. 

### \<label\>
- form에 question을 추가할 수 있음. 
- for 속성으로 input의 id를 지정해주어 사용가능. 
- for 와 같은 값을 갖는 input을 작동시켜줌.  

### id 
- body 안의 어떤 태그에도 넣을 수 있는 속성
- 요소 하나당 하나의 id만 가질 수 있음.


## Semantic HTML

### div (division) -> 박스의 개념.
- 태그를 구분해서 배치할 떄 사용
- div는 코드 자체로는 의미없는 구분
- 의미가 있는 div역할을 하는 태크들이 존재.
### \<header\> 
- div랑 같은 역할이지만 머릿말에 부분에 사용
### \<main\>
- div랑 같은 역할이지만 본문에 부분에 사용
### \<footer\>
- div랑 같은 역할이지만 꼬릿말에 부분에 사용
### \<span\> 
- 짧은 text를 위한 태그. 요소 자체로는의미가 없음

<br/><br/><br/>
	
	
# 3강 (CSS)
	
# CSS의 두가지 방법
1. HTML 과 CSS 같은 파일에
- \<head\>안에서 \<style\>태그를 사용. 

2. HTML 과 CSS 다른 파일로 분리
```
<link href="url" rel="stylesheet"/> 태그를 통해서 CSS파일 불러오기 
```
 cf) rel = relationship

# Writing Our First CSS Lines
 
 cf) CSS의 속성은 property라고 부름 
 cf) HTML의 속성은 attribute

 - 셀렉터를 지정, 셀렉터 안에 속성 을 명시.

 ``` html
<style>
	selector{ 
		property:value;
		font-size:20px;
	}
</style>
 
 ```

# Cascading의 뜻
: 브라우저가 CSS코드를 읽을 때 위에서부터 차례로 읽는다는 말.

- 같은 셀렉터가 설정되어있으면 마지막 설정이 브라우저에 표현 됨. 


# 3-3 강 Box(Blocks) and Inlines
- box를 만들면 박스 옆에 또다른 박스가 오지 않음.
cf) 다른 태그들은 기본적으로 옆에 배치
### Blocks
: 옆에 다른 요소가 못 오는 것을 block(box)
### Inlines
: 옆에 다른 요소가 올 수 있는 것을 inline

# 3-5 강 Collapsing margins
- 하나의 box의 경계가 다른 box의 경계와 같다면 두 margin은 하나로 취급된다. -> 경계가 만나면 하나로 취급. 
- 위, 아래쪽에서만 일어남.  
- 이를 해결하기 위해 padding이라는 개념이 등

# 3.6 Paddings and IDs

### padding 
: box의 경계로부터 '안쪽'에 있는 공간

cf) margins
: box의 경계로부터 '바깥쪽'에 있는 공간


### css에서 id로 지정
#first{ (id="first")
         
      }


# 3.7 Border
- 거의 한 종류의 보더만 사용.

*{ (모든 요소에 지정)
	
} 

- inline에도 border 지정 가능. 

# 3.8 classes
cf) inline일 경우 넓이와 높이를 가질 수 없기 때문에 -> margin이 좌우만 적용 됨., padding은 상하좌우 적용. 

ex)

``` CSS
#tomato, #tomato2, #tomato3{
        background-color: tomato;
      }
```
- 요소를 가리킬 수 있으면서도 겹쳐도 되는 방법 -> class

``` CSS
.tomato{
	
}	

	<span class = "tomato">hello</span>
    <span class = "tomato2">hello</span>
    <span class = "tomato3">hello</span>
```
- 클래스 이름은 중복으로 적용 가능. 
 
# 3.9 Inline Block
- inline block은 
-> 높이와 넓이를 갖으면서 좌우 margin갖음.
-> 요소 옆에 다른 요소가 올 수도 있음
- display:inline-block;
- 깔끔하지 못함.(반응형 디자인을 반영 못함)

# 3.10 Flexbox Part One
- 부모 엘리멘트만 명시해야한다.
-> flex 부모 
```CSS
body{
display : flex;
justify-content: ~;
}
```
-> 계산을 자동으로

- justify-content -> main axis
- align-items -> cross axis

vh = Viewport Height

# 3.12 Fixed 
- ponsiton:fixed
``` CSS
div{
      position : fixed;
}
```
-> 다른 레어어를 부수고 가장 위의 레이어에 위치하게 됨.

# 3.13 Relative Absolute
- position : static (디폴트)

- position : relative;
-> top bottom left right속성 사용가능

``` CSS
.green{
   position: relative;
   top:-10px    
}
```
-> 처음 위치한 곳을 기준으로 수정하는 것. 


- position : absolute;
-> relative한 부모 기준으로 맨 끝쪽으로 가게 위치 시킴(부모가 relative아니면 body가 relative부모가 됨)

#3.14 Pseudo Selectors part One
``` CSS
div:first-child{
      background-color: tomato;
}
div:last-child{
      background-color: teal;
}
span:nth-child(2){
      background-color: teal;     
}
span:nth-child(even){
      background-color: teal;     
}
span:nth-child(2n+1){
      background-color: teal;     
}
```

# 3.15 Combinators
``` CSS
p span{ 
      color:teal;
}

<span>hello</span>
<p> lorem ipsum 
      <span>inside</span>
</p> 
```
- 부모인 p를 쓴다음 span을 씀.

``` CSS
div > span{
      text:decoration: underline;
}
```
- direct children -> 바로 밑 자식에게만 적용

``` CSS
p + span{
       text-decoration: underline;     
}
```
- 형제 요소를 지정할 때. 

# 3.16 Pseudo Selectors part Two
``` CSS
p ~ span{
        text-decoration: underline;          
}
```
- 형제관계 (바로 옆에 없어도 됨.)
 
``` CSS
input{
      border: 1px solid wheat
}

input:required{
      border:1px solid tomato;
}

input 
```

### attribute selector
- attribute를 통해 어떤 것이든 선택할 수 있음
``` CSS
input[type="password"]{
      background-color: thistle;
} 
input[placeholder~="name"]{
      background-color:tomato;
}
<input type="text" placeholder="First name"/>
<input type="text" placeholder="Last name"/>
```
- *= "str"
-> 아무 글자들 사이에서 부분적으로 포함하는 값 찾아서 지정
- \~= "str" 
-> 앞뒤에 공백이 있는 상태에서 부분적으로 포함하고 있는 값을 찾아서 지정
- $="str"
-> 끝나는 단어를 찾아서 지정.

#. 3.17 States 
- active 
``` CSS
button:active{
	background-color:tomato;	
}
```
- hover
: 마우스가 커서 위에 있을 때. 
button:hover{
	background-color:tomato;	
}

- focus
: 키보드나 마우스로 선택되었을 때
button:focus{
	background-color:tomato;	
}

- visited
: 링크를 방문했던 경우
 a:focus{
	background-color:tomato;	
}

- focus-within
: focus-within은 focused인 자식을 가진 부모 엘리먼트의 상태 
form:focus-within{
	background-color:tomato;	
}

### state를 다른 엘리먼트와 chain해서 사용가능
```CSS
form:hover input{
	background-color:white;
}
```
- form이 hover가 되어있고 그 안에 input이 있을 떄 적용 됨. 
```CSS
form:hover input:focus{
	background-color:white;
}
```
- - form이 hover가 되어있고 그 안에 input이 focus 되어 있을 떄 적용 됨. 


# 3.18 Recap

cf) 수도 엘리먼트 중 ::placeholder
-> placeholder 꾸미기

``` CSS
input :: placeholder{
	color:white;
}
```
-> input의 placeholder를 꾸며준다. 

### selection
``` CSS
p::selection
background-color:grenn;
```
-> 텍스트를 셀렉트하면 표현됨. 

# 3.19 Colors and Variables
cf) background-colo:rgba(레드, 그린, 블루, 투명도);

### :root
- 모든 엘리먼트의 부모 
```CSS
:root{
	--main-color: #fcce00;
	(변수 생성하는 작업)
}
p{
	color:var(--main-color);
}
```

# 고급 CSS
# 4.0 Transitions 
- 어떤 상태에서 다른 상태로 가는 변화를 애니메이션화. 
- transition이라는 속성은 state가 없는 요소에 붙어야함.
``` CSS
a{
	transition: background-color 10s ease-in-out; 
}
a:hover{
	color: tomato;
	background-color: wheat;
}
- 변하게 될 속성을 지정.
```

# 4.1 Transitions part Two
### ease-in function
- 내장 애니메이션 함수
### cubiz-bezier
- 직접 만드는 애니메이션 함수

# 4.2 Transformations
``` CSS
ims{
	transform:rotateY(85deg) rotateX(20deg); rotateZ(20deg);
}
```
-> 3d 작업을 할 수 있음.(픽셀변형)
-> siblings에 영향을 미치지 않음.
-> 다른 box element에 영향X. 

# 4.3 Animations part One
- 애니메이션은 우리가 원하는 만큼 자동적으로 재생할 수 있음.
``` CSS
@keyframes superSexyCoinFlip{
	from{
		transform:rotateX(0);
	}
	to{
	transform:rotateY(180deg) translateX(100px);
	}
}
img{
	animation: superSexyCoinFlip 5s ease-in-out; 
}
```

# 4.4 Animations part Two
```CSS
@keyframes superSexyCoinFlip{
	0%{
		transform:rotateX(0);
	}
	50%{
	transform:rotateY(180deg) translateX(100px);
	}
	100%{
		transform: rotateY(0);
	}
}
img{
	animation: superSexyCoinFlip 5s ease-in-out; 
}
``` 

# 6.0 Introduction

- .gitignore -> 무시하고 싶은 파일이름을 기록하는 곳.

# 6.2 BEM (Block Element modifier)
- modifier -> --orange (\_\_가 아니라 --)

``` html
<a class ="btn btn--bif btn--orange" href="https://css-tricks.com">
	<span class="btn__price">$9.99</span>
	<span class="btn__text">Subscribe</span>
</a>
```

-> btn__price -> 버튼 밑에 price span
-> btn--bif -> 큰 버튼 


# 6.3 Font Awesme
- svg 수학적으로 표현된 이미지파일. 
: heroicons -> 아이콘 모아둔 사이트. 
: FontAwesome -> 폰트, 아이콘. 

# 6.5 Status Bar CSS 
### font-family:
``` CSS
body{
	font-family:Oxygen;
}

```

### css hack
- 요소 중심에 맞추는 하나의 방식
``` CSS
.status-bar {
  display: flex;
  justify-content: center;
}

.status-bar__column:first-child span {
  margin-right: 5px;
  width: 33%;
}

.status-bar__column:nth-child(2) {
  display: flex;
  justify-content: center;
}

.status-bar__column:last-child {
  display: flex;
  justify-content: flex-end;
  align-items: center;
}

``` 
