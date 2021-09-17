# about_HTML_CSS
HTML과 CSS를 공부하며 알게 된 것들을 기록하는 저장소입니다.

# tags 
### \<label\>
- 라벨 요소는 for 속성을 사용하여 다른요소와 결합 가능. for의 값은 다른 요소의 id 값. 라벨을 결합하고자 하는 요소 내부에 위치시키면 for사용 안해도 결합 가능.
- 브라우저에 의해 일반적인 텍스트로 렌더링되지만, 마우스로 클릭할 경우 라벨과 연결된 요소를 곧바로 선택할 수 있음.
- 라벨을 요소로 사용할 수 있는 요소들
: \<button\>, \<input\>, \<meter\>, \<output\>, \<progress\>, \<select\>, \<textarea\>


### \<select\>
- name 속성 : 드롭다운 리스트의 이름을 명시. + 폼(form)이 제출된 후 서버에 폼 데이터를 참조하기 위해 사용되거나, 자바스크립트에서 요소를 참조하기 위해 사용됨.

### \<option\>
: value 속성 : 폼을 제풀할 때 서버로 보내지는 값. value속성이 명시되지 않으면 해당 값은 옵션 요소 내의 텍스트로 자동 설정됨.






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
### \<input \/\>
-  속성들
: type -> 기본값은 text. ...
: type = "file" -> accept로 파일 종류 제한 가능  
: placeholder -> 인풋 미리 채워줌 
: required -> 반드시 채워야 함. 

### \<label\>
- form에 question을 추가할 수 있음. 
- for 속성으로 input의 id를 지정해주어 사용가능. 
- for 와 같은 값을 가능 input을 작동시켜줌.  

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
