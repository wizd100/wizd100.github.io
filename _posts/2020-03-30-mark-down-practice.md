---
title:  "마크다운 문법 사용법 및 테스트"
comments: true
read_time: false
---

## 목차
* TOC
{:toc}

헤더를 읽어들여서 자동으로 목차를 생성함

```
* TOC
{:toc}
```

## 헤더 (제목)
# 헤더1
## 헤더2
### 헤더3
#### 헤더4
##### 헤더5
###### 헤더6

```
# 헤더1
## 헤더2
### 헤더3
#### 헤더4
##### 헤더5
###### 헤더6
```

jekyll minima 테마에서 h2가 h1보다 크게 보이는건 h1이 제목에 사용되기 때문?

[참고링크](https://github.com/jekyll/minima/issues/113)

## 인용문
> 1
>> 2
>>> 3

```
> 1
>> 2
>>> 3
```

## 숫자 목록
1. 숫자 목록1
    1. 숫자 목록 1-1
        1. 숫자 목록 1-1-1
    3. 숫자 목록 1-2 
2. 숫자 목록2
3. 숫자 목록3

```
1. 숫자 목록1
    1. 숫자 목록 1-1
        1. 숫자 목록 1-1-1
    3. 숫자 목록 1-2 
2. 숫자 목록2
3. 숫자 목록3
```
1,2,3 순서대로 쓰지 않아도 자동으로 순서대로 번호를 붙임

## 목록
* 1
    * 1-1
* 2
* 3 

- 1
    - 1-1
- 2
- 3

+ 1
+ 2
    + 2-1
+ 3

```
* 1
    * 1-1
* 2
* 3 

- 1
    - 1-1
- 2
- 3

+ 1
+ 2
    + 2-1
+ 3
```

*, -, + 셋다 똑같이 보이기 때문에 아무거나 써도 될 듯

## 코드블럭
    jekyll serve

띄어쓰기 4번 또는  ``` <pre></pre>

* ```java 해당언어에 맞게끔 지정해주면 자동으로 코드 강조를 해줌 (java, php, c...)

```java
System.out.print("Hello");
```

```
```java
System.out.print("Hello");
```


## 인라인 코드
``` <code>123</code> ```

<code>123</code>

## 강조
*asterisks*

_underscore_

**asterisks 강조**

__underscore 강조__

~~취소선~~

<u>밑줄</u>

    *asterisks*
    
    _underscore 강조_
    
    **asterisks 강조**
    
    __underscore__
    
    ~~취소선~~
    
    <u>밑</u>

## 링크
[구글](https://www.google.co.kr/)

[구글][1]

[1]: https://www.google.co.kr/

<https://www.google.co.kr/>

[구글](https://www.google.co.kr/){:target="_blank"}

    <!-- 글자에 링크를 추가 -->
    [구글](https://www.google.co.kr/)
    
    <!-- 참조 링크 -->
    [구글][1]
    
    [1]: https://www.google.co.kr/
    
    <!-- 꺽쇠로 링크 -->
    <https://www.google.co.kr/>
    
    <!-- 링크를 새창에서 띄우고 싶을때 -->
    [구글](https://www.google.co.kr/){:target="_blank"}
    
## 이미지
![대체 텍스트](/assets/doge.jpg)

![대체 텍스트](/assets/doge.jpg "타이틀 옵션")

[![대체 텍스트](/assets/doge.jpg)](https://www.google.co.kr/search?q=doge)

![대체 텍스트](/assets/doge.jpg){:width="100px" height="300px"}

<img src="/assets/doge.jpg">

    <!-- 이미지 -->
    ![대체 텍스트](/assets/doge.jpg)
    
    <!-- 타이틀 속성 -->
    ![대체 텍스트](/assets/doge.jpg "타이틀 옵션")
    
    <!-- 이미지에 링크 -->
    [![대체 텍스트](/assets/doge.jpg)](https://www.google.co.kr/search?q=doge)
    
    <!-- 이미지 크기 조절 -->
    ![대체 텍스트](/assets/doge.jpg){:width="100px" height="300px"}
    
    <!-- 이미지 태그를 이용해도 됨 -->
    <img src="/assets/doge.jpg">
    
## 수평선
123
<hr>
123
* * *
123
- - -

    123
    <hr>
    123
    * * *
    123
    - - -
    
## 테이블

| a  | b  | c  |
|---|:---:|---:|
| 1  | 2  | 3  |
| 4  | 5 | 6  |
| 7  | 8 |  9 |

    <!-- 테이블 헤더부분 -->
    | a  | b  | c  |
    
    <!-- 헤더와 값 구분  ':'추가함으로써 정렬가능 -->
    |---|:---:|---:|
    
    | 1  | 2  | 3  |
    | 4  | 5 | 6  |
    | 7  | 8 |  9 |


    