# Markdown
```Markdown�� �Ϲ� �ؽ�Ʈ ����� �淮 ��ũ�� ����̴�.```
****
# **1. ��ũ�ٿ��̶�?**
## **1.1. ��ũ�ٿ� �Ұ�**
�Ϲ� �ؽ�Ʈ�� ������ �ִ� ������ �ۼ��ϴ� �� ���Ǹ�, �Ϲ� ��ũ�� �� ���� ������ ���� ������ ���� Ư¡�̴�. HTML �� ���� ������ ���� ��ȯ�� �� �ִ�. �ֱ� ��ũ�ٿ��� �����ޱ� ������ ������ ���� �����̴�. ������ ����� Repository�� ���� ������ ����ϴ� README.md�� ������ ����ϴ� ����̶�� ������ ���� ���� ���ϰ� �Ǵ� ��ũ�ٿ� �������µ�, �� ��ũ�ٿ��� ���ؼ� ��ġ ���, �ҽ��ڵ� ����, �̽� ���� �����ϰ� ����ϰ� �������� ���� �� �ִٴ� ������ �ΰ��Ǹ鼭 ���� ���� ������ ���������� �Ǿ���.
****
## **1.2. ��ũ�ٿ��� �����**
### ����
        1. �����ϴ�.
        2. ������ �������� �ۼ������ϴ�.
        3. �پ��� ���·� ��ȯ�� �����ϴ�.
        4. �ؽ�Ʈ�� ����Ǳ� ������ �뷮�� ���� ������ �����ϴ�.
        5. �ؽ�Ʈ�����̱� ������ �������� �ý����� �̿��Ͽ� �����̷��� ������ �� �ִ�.
        6. �����ϴ� ���α׷��� �÷����� �پ��ϴ�.
### ����
        1. ǥ���� ����.
        2. ��� HTML ��ũ���� ������� ���Ѵ�.
****
# **2. ��ũ�ٿ� ����**
## **2.1. ����**
* '#'�� ����ϴ� ���
```
# ������
### 1������
###### 6������ �����ϴ�.
```

* '---'�Ǵ� '===' ���
```
����
====
������
---
```

## **2. ���**
* ������ �ִ� ���
```
1. ù��°
2. �ι�°
3. ����°
```
1. ù��°
2. �ι�°
3. ����°

* ������ ���� ��� (*, +, -)
```
* 1����
    + 1-1����
    + 1-2����
* 2����
```
* 1����
    + 1-1����
    + 1-2����
* 2����
## **3. �ο빮��**
```
> blockQuote
>   >blockQuote
```
> blockQuote
>   >blockQuote
## **4. �ڵ� ����**
* '```' ���
<br>
git hub������ �ڵ� �������� ����ϴ� �� �����Ͽ� ���������� �����ϴ�. (�ʼ��� �ƴ�)
<pre>
```
�ڵ��..
```
</pre>

* 'pre'�±� ���
```
<pre>
<code>
�ڵ��..
</code>
</pre>
```

## **5. ����**
```
***
-----
<hr/>
```
***
-----
<hr/>

## **6. ����(*, _ ���)**
```
*���¸�ü*
**����ü**
***���¸� + ����ü***
~~��Ҽ�~~
```
*���¸�ü* <br>
**����ü** <br>
***���¸�+����ü*** <br>
~~��Ҽ�~~

## **7. ����**
���⸦ ������ &nbsp;&nbsp;&nbsp;������ �ϰ� �ʹٸ� 
```
&nbsp;&nbsp;&nbsp;
```

## **8. �ٹٲ�**
```
���� ���������� ��ĭ ���⸦ �ϸ� �ȴ�.   
Ȥ�� <br> 
Ȥ�� <p> </p>�� ����ϸ� �ȴ�.
```
���� ���������� ��ĭ ���⸦ �ϸ� �ȴ�.   
Ȥ�� <br> 
Ȥ�� <p> </p>�� ����ϸ� �ȴ�.

## **9. ��ũ**
* ���� ��ũ
```
Link1 : [Google][googlelink]

[googlelink]: https://google.com "Go google"

```
Link1 : [Google][googlelink]

[googlelink]: https://google.com "Go google"

* �ζ��� ��ũ (= �ܺθ�ũ)
```
Link1 : [Google](https://google.com, "google link") 
<br>
Link2 : <a href="https://www.naver.com" target="_blank" title="���̹�">naver</a>

```
Link1 : [Google](https://google.com, "google link") <br>
Link2 : <a href="https://www.naver.com" target="_blank" title="���̹�">naver</a>

* URL ��ũ, e-mail ��ũ
```
URL ��ũ: <http://example.com/>
<br>
�̸��ϸ�ũ: <address@example.com>
```
URL ��ũ: <http://example.com/> <br>
�̸��ϸ�ũ: <address@example.com>

* �ٸ� md ���Ϸ� �̵�

��� ��θ� �̿��ؾ��Ѵ�.   

ex1) ���� ��ġ�� ETC������ markdown.md ���Ͽ��� ������ README.md�� �̵��ϰ� �ʹٸ�? 
```
[README.md�� �̵�](../README.md)
```
[README.md�� �̵�](../README.md)   

ex2) ���� ��ġ�� ETC������ markdown.md ���Ͽ��� spring�� controller/ HttpServletRequest, HttpServletResponse.md�� �̵��ϰ� �ʹٸ�? 
```
[controller�� �̵�](../Spring/Controller/HttpServletRequest, HttpServletResponse.md)
```
[controller�� �̵�](../Spring/Controller/HttpServletRequest.md)

* ���� md���� �ȿ����� �̵�
```
[���� md���� �ȿ��� �̵�](#9.-��ũ)
������ �� : ������ -���ιٲ۴�.
�̸���, ��ħǥ(.), �޸�(,)���� 
```
[���� md���� �ȿ��� �̵�](#9.-��ũ)

<br>

## **10. �̽������� ����**
```
\### ���
### ���
```
\### ���
### ���
<br>

## **11. �̸�Ƽ��**
* üũ�ڽ�
```
    * [] �� üũ�ڽ�
    * [X] üũ�ڽ�
```
    + [] �� üũ�ڽ�
    + [X] üũ�ڽ�

* �̸���
���� ����ϴ� �� : ???????????????
https://gist.github.com/rxaviers/7360908

<br>

## **13. ���**
<details>
<summary>����ϱ�</summary>

Ŭ���ÿ��� ����ϱ���     
������ ��ϴ�!
</details>

<br>

```
<details>
<summary>����ϱ�</summary>

Ŭ���ÿ��� �����     
������ ��ϴ�!
</details>
```

## **12. �̹���**
```
!�� �̿��ϸ�ȴ�.
![���ڽ� ������ �̹�����](�̹����ּ�)(��ũ�ּ�)

![���Ͽ�](https://photo.newsen.com/mphoto/2019/07/06/201907062110193510_1.jpg "���Ͽ�")

<img src="https://photo.newsen.com/mphoto/2019/07/06/201907062110193510_1.jpg" width="100px" height="100px" title="px(�ȼ�) ũ�� ����" alt="���Ͽ�"/>
```

![���Ͽ�](https://photo.newsen.com/mphoto/2019/07/06/201907062110193510_1.jpg "���Ͽ�")
<img src="https://photo.newsen.com/mphoto/2019/07/06/201907062110193510_1.jpg" width="100px" height="100px" title="px(�ȼ�) ũ�� ����" alt="���Ͽ�"/>

�̹����� src�� ��� ���� ���� �ణ�� Ʈ���� ����� �� �ִ�.
�ٷ� github ������Ʈ�� Issue�� �̿��ϴ� ���̴�. �� ������� �̹��� �Ӹ��ƴ϶� ������ �߰��� �� �ִ�.
```
1. github ������Ʈ�� Issue������ ����.
2. New Issue ��ư
3. ������ϴ� �̹����� �巡�� �� ���
4. "<img src=~~>" ������ ���ڿ��� ��ȯ�ȴ�. �̸� ����ϸ�ȴ�.
```
<br>

## **13. ���̺�**
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