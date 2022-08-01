# HTML

## HTML 기본 형태

```
<!DOCTYPE HTML>
<html>
    <head>
        <meta charset="UTF-8"/>
        <title> WEB TITLE </title>
    </head>
    <body>
    </body>
</html>
```
!DOCTYPE HTML은 이 문서에는 HTML이 담겨있다는 뜻으로 관용적으로 사용한다. 그 밑에는 html태그로 head와 body태그를 감싸고 있다. head에는 웹페이지의 제목인 title태그와 charset 등을 선언해줄 수 있는 meta태그가 있다.

<hr>

## 줄바꿈 태그

* br

```
<br>
```
가장 대표적으로 줄바꿈을 하기위해 사용하는 태그이다. 줄바꿈이라는 시각적인 의미만을 가지고 있기 때문에 뭔가를 감쌀 필요가 없다.

* p
```
<p> </p>
```
Paragraph의 앞글자를 따서 p 태그를 사용한다. 단락으로 묶기 때문에 p 태그는 br태그와 다르게 어디까지가 한 단락인지를 표현할 수 있기 때문에 열리는 태그와 닫히는 태그가 존재한다. 

>p 태그와 br 태그를 비교했을 때 p 태그는 정해진 여백만큼 벌어지기 때문에 시각적으로 자유도가 떨어진다. 이럴때 CSS 문법을 사용하게 된다. 나중에 천천히 배우겠지만, 단락과 단락사이의 여백을 더 주고 싶을때 예를 들어 밑에 단락의 p태그에 아래와 같이 작성하면 된다.
```
<p style="margin-top:40px;"> ... </p>
```

<hr>

## 이미지 태그
```
<img src="경로" width="">
```

경로에는 인터넷에서 이미지 주소 복사를 해서 붙여넣어도 되고, 파일의 로컬 경로를 넣어도 좋다. width는 기본적으로 100%로, 해당 속성을 쓸 경우 상대적으로 크기가 변한다.

<hr>

## 목록 태그

목록을 작성할때 단순하게 한 줄씩 쓰고 br태그를 사용할 수도 있지만 이건 의미에 맞게 사용된 것이 아니다. 이럴때는 li 태그를 사용한다.
```
<li>1</li>
<li>2</li>
<li>a</li>
<li>b</li>
```
<li>1</li>
<li>2</li>
<li>a</li>
<li>b</li>

이 때, 리스트를 여러개를 붙이게 될 경우 구분이 가지 않기 때문에 띄어쓰기를 하고싶다. <br> 이때 사용하는 것이 li의 태그의 부모인 ul 태그이다.
```
<ul>
    <li>1</li>
    <li>2</li>
</ul>
<ul>
    <li>a</li>
    <li>b</li>
</ul>
```
<ul>
    <li>1</li>
    <li>2</li>
</ul>
<ul>
    <li>a</li>
    <li>b</li>
</ul>

> 즉, li 태그는 어디서부터 어디까지가 연관된 항목인지 구분하기 위한 부모 태그가 반드시 필요하다. ul은 Unordered이고, ol은 Oldered이다. 

<hr>

## 테이블 태그

테이블을 만들 때에도 리스트와 동일하게 부모 속성을 사용한다. table태그 안에 tr(table row)로 행의 개수를 정하고, 그 안에서 td로 열의 개수만큼 선언한다.
```
<table>
    <tr>
        <td>head</td>
        <td>98.1%</td>
    </tr>
    <tr>
        <td>body</td>
        <td>97.9%</td>
    </tr>
    <tr>
        <td>html</td>
        <td>97.9%</td>
    </tr>
</table>
```
<table>
    <tr>
        <td>head</td>
        <td>98.1%</td>
    </tr>
    <tr>
        <td>body</td>
        <td>97.9%</td>
    </tr>
    <tr>
        <td>html</td>
        <td>97.9%</td>
    </tr>
</table>

<hr>

## 링크 태그

링크 태그는 Anchor의 첫 글자를 딴 a태그를 이용한다. 

```
<a href="https://www.w3.org/TR/html5/" target="_blank" title="specification"> ... </a>
```

### 속성

<table>
    <tr>
        <td>href</td>
        <td>Hypertext의 h와 Reference의 ref를 딴 href 속성을 사용하여 닻을 내릴 링크를 내린다.</td>
    </tr>
    <tr>
        <td>target</td>
        <td>_blank로 새 탭에서 열릴 수 있게 해준다.</td>
    </tr>
    <tr>
        <td>title</td>
        <td>링크에 커서를 올리면 나타는 툴팁을 제시할 수 있다.</td>
    </tr>
</table>

