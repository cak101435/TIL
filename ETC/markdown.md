# Markdown
```Markdown은 일반 텍스트 기반의 경량 마크업 언어이다.```
****
# **1. 마크다운이란?**
## **1.1. 마크다운 소개**
일반 텍스트로 서식이 있는 문서를 작성하는 데 사용되며, 일반 마크업 언어에 비해 문법이 쉽고 간단한 것이 특징이다. HTML 등 서식 문서로 쉽게 변환될 수 있다. 최근 마크다운이 각광받기 시작한 이유는 깃헙 덕분이다. 깃헙의 저장소 Repository에 관한 정보를 기록하는 README.md는 깃헙을 사용하는 사람이라면 누구나 가장 먼저 접하게 되는 마크다운 문서였는데, 이 마크다운을 통해서 설치 방법, 소스코드 설명, 이슈 등을 간단하게 기록하고 가독성을 높일 수 있다는 강점이 부각되면서 점점 여러 곳으로 퍼져나가게 되었다.
****
## **1.2. 마크다운의 장단점**
### 장점
        1. 간결하다.
        2. 별도의 도구없이 작성가능하다.
        3. 다양한 형태로 변환이 가능하다.
        4. 텍스트로 저장되기 때문에 용량이 적어 보관이 용이하다.
        5. 텍스트파일이기 때문에 버전관리 시스템을 이용하여 변경이력을 관리할 수 있다.
        6. 지원하는 프로그램과 플랫폼이 다양하다.
### 단점
        1. 표준이 없다.
        2. 모든 HTML 마크업을 대신하지 못한다.
****
# **2. 마크다운 문법**
## **2.1. 제목**
* '#'를 사용하는 방법
```
# 제목은
### 1개부터
###### 6개까지 가능하다.
```

* '---'또는 '===' 사용
```
제목
====
부제목
---
```

## **2. 목록**
* 순서가 있는 목록
```
1. 첫번째
2. 두번째
3. 세번째
```
1. 첫번째
2. 두번째
3. 세번째

* 순서가 없는 목록 (*, +, -)
```
* 1번글
    + 1-1번글
    + 1-2번글
* 2번글
```
* 1번글
    + 1-1번글
    + 1-2번글
* 2번글
## **3. 인용문구**
```
> blockQuote
>   >blockQuote
```
> blockQuote
>   >blockQuote
## **4. 코드 삽입**
* '```' 사용
<br>
git hub에서는 코드 시작점에 사용하는 언어를 선언하여 문법강조가 가능하다. (필수는 아님)
<pre>
```
코드들..
```
</pre>

* 'pre'태그 사용
```
<pre>
<code>
코드들..
</code>
</pre>
```

## **5. 수평선**
```
***
-----
<hr/>
```
***
-----
<hr/>

## **6. 강조(*, _ 사용)**
```
*이태릭체*
**볼드체**
***이태릭 + 볼드체***
~~취소선~~
```
*이태릭체* <br>
**볼드체** <br>
***이태릭+볼드체*** <br>
~~취소선~~

## **7. 띄어쓰기**
띄어쓰기를 여러번 &nbsp;&nbsp;&nbsp;적용을 하고 싶다면 
```
&nbsp;&nbsp;&nbsp;
```

## **8. 줄바꿈**
```
문장 마지막에서 세칸 띄어쓰기를 하면 된다.   
혹은 <br> 
혹은 <p> </p>를 사용하면 된다.
```
문장 마지막에서 세칸 띄어쓰기를 하면 된다.   
혹은 <br> 
혹은 <p> </p>를 사용하면 된다.

## **9. 링크**
* 참조 링크
```
Link1 : [Google][googlelink]

[googlelink]: https://google.com "Go google"

```
Link1 : [Google][googlelink]

[googlelink]: https://google.com "Go google"

* 인라인 링크 (= 외부링크)
```
Link1 : [Google](https://google.com, "google link") 
<br>
Link2 : <a href="https://www.naver.com" target="_blank" title="네이버">naver</a>

```
Link1 : [Google](https://google.com, "google link") <br>
Link2 : <a href="https://www.naver.com" target="_blank" title="네이버">naver</a>

* URL 링크, e-mail 링크
```
URL 링크: <http://example.com/>
<br>
이메일링크: <address@example.com>
```
URL 링크: <http://example.com/> <br>
이메일링크: <address@example.com>

* 다른 md 파일로 이동

상대 경로를 이용해야한다.   

ex1) 현재 위치인 ETC파일의 markdown.md 파일에서 상위의 README.md로 이동하고 싶다면? 
```
[README.md로 이동](../README.md)
```
[README.md로 이동](../README.md)   

ex2) 현재 위치인 ETC파일의 markdown.md 파일에서 spring의 controller/ HttpServletRequest, HttpServletResponse.md로 이동하고 싶다면? 
```
[controller로 이동](../Spring/Controller/HttpServletRequest, HttpServletResponse.md)
```
[controller로 이동](../Spring/Controller/HttpServletRequest.md)

* 같은 md파일 안에서의 이동
```
[같은 md파일 안에서 이동](#9.-링크)
주의할 점 : 공백은 -으로바꾼다.
이모지, 마침표(.), 콤마(,)생략 
```
[같은 md파일 안에서 이동](#9.-링크)

<br>

## **10. 이스케이프 문자**
```
\### 출력
### 출력
```
\### 출력
### 출력
<br>

## **11. 이모티콘**
* 체크박스
```
    * [] 빈 체크박스
    * [X] 체크박스
```
    + [] 빈 체크박스
    + [X] 체크박스

* 이모지
많이 사용하는 건 : ???????????????
https://gist.github.com/rxaviers/7360908

<br>

## **13. 요약**
<details>
<summary>요약하기</summary>

클릭시에는 요약하기의     
설명이 뜹니다!
</details>

<br>

```
<details>
<summary>요약하기</summary>

클릭시에는 요약의     
설명이 뜹니다!
</details>
```

## **12. 이미지**
```
!를 이용하면된다.
![엑박시 보여질 이미지명](이미지주소)(링크주소)

![송하영](https://photo.newsen.com/mphoto/2019/07/06/201907062110193510_1.jpg "송하영")

<img src="https://photo.newsen.com/mphoto/2019/07/06/201907062110193510_1.jpg" width="100px" height="100px" title="px(픽셀) 크기 설정" alt="송하영"/>
```

![송하영](https://photo.newsen.com/mphoto/2019/07/06/201907062110193510_1.jpg "송하영")
<img src="https://photo.newsen.com/mphoto/2019/07/06/201907062110193510_1.jpg" width="100px" height="100px" title="px(픽셀) 크기 설정" alt="송하영"/>

이미지의 src를 얻어 내기 위해 약간의 트릭을 사용할 수 있다.
바로 github 프로젝트의 Issue를 이용하는 것이다. 이 방법으로 이미지 뿐만아니라 동영상도 추가할 수 있다.
```
1. github 프로젝트의 Issue탭으로 들어간다.
2. New Issue 버튼
3. 얻고자하는 이미지를 드래그 앤 드랍
4. "<img src=~~>" 형식의 문자열로 반환된다. 이를 사용하면된다.
```
<br>

## **13. 테이블**
```
<!-- Markdown -->
Title1|Title2
-|-
content1|content2
content3|content4
  
Title1|Title2|Title3
:-|:-:|-:
content1|content2|content3
<!-- Html -->
<figure>
    <table>
        <thead>
            <tr>
                <th>Title1</th>
                <th>Title2</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>content1</td>
                <td>content2</td>
            </tr>
            <tr>
                <td>content3</td>
                <td>content4</td>
            </tr>
        </tbody>
    </table>
</figure>
  
<figure>
    <table>
        <thead>
            <tr>
                <th style='text-align:left;' >Title1</th>
                <th style='text-align:center;' >Title2</th>
                <th style='text-align:right;' >Title3</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td style='text-align:left;' >content1</td>
                <td style='text-align:center;' >content2</td>
                <td style='text-align:right;' >content3</td>
            </tr>
        </tbody>
    </table>
</figure>
```
<!-- Markdown -->
Title1|Title2
-|-
content1|content2
content3|content4
  
Title1|Title2|Title3
:-|:-:|-:
content1|content2|content3
<!-- Html -->
<figure>
    <table>
        <thead>
            <tr>
                <th>Title1</th>
                <th>Title2</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>content1</td>
                <td>content2</td>
            </tr>
            <tr>
                <td>content3</td>
                <td>content4</td>
            </tr>
        </tbody>
    </table>
</figure>
  
<figure>
    <table>
        <thead>
            <tr>
                <th style='text-align:left;' >Title1</th>
                <th style='text-align:center;' >Title2</th>
                <th style='text-align:right;' >Title3</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td style='text-align:left;' >content1</td>
                <td style='text-align:center;' >content2</td>
                <td style='text-align:right;' >content3</td>
            </tr>
        </tbody>
    </table>
</figure>