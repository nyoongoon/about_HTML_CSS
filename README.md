# about_HTML_CSS
HTML과 CSS를 공부하며 알게 된 것들을 기록하는 저장소입니다.

# 1강 (HTML) 
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

# 3-6 강 Paddings and IDs 
- padding은 box의 경계로부터 '안쪽'에 있는 공간.
cf) margin은 box의 경계로부터 '바깥'에 있는 공간.
