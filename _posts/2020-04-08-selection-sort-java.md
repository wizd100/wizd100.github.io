---
layout: post
title:  "선택정렬(Selection sort) java 소스코드"
permalink: /:categories/:year/:month/:day/:title/
date:   2020-04-08 17:20:00 +0900
categories: posts
tags: [정렬, 알고리즘, java]
use_math: true
---

<iframe width="100%" height="500" src="https://www.youtube.com/embed/Ns4TPTC8whw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## 선택정렬이란?
값들 중에서 가장 최소값을 찾아서 맨 왼쪽으로 채워가면서 정렬하는 방법

    예제 : 오름차순으로 선택정렬 
    10 5 3 1 7 - 시작
    10 5 3 1 7 - 최소값 1을 찾음
    1 5 3 10 7 - 1과 첫번째 값인 10을 교환 후 패스
    1 5 3 10 7 - 최소값 3을 찾음 (첫번째 값은 제외하고 찾음)
    1 3 5 10 7 - 3과 두번째 값인 5를 교환 후 패스 (첫번째 값은 제외하고 교환)
    1 3 5 10 7 - 최소값 5를 찾음
    1 3 5 10 7 - 세번째에 있음으로 교환없이 패스
    1 3 5 10 7 - 최소값 7을 찾음
    1 3 5 7 10 - 최소값 7과 10을 교환 후 정렬 완료 
    
## 선택정렬 특징
- 장점
    - 구현이 간단하다
- 단점
    - 데이터가 클 수록 느려짐


## 시간복잡도
- 최악 시간복잡도 : $$O(n^2)$$ 비교, $$O(n)$$ 교환
- 최선 시간복잡도 : $$O(n^2)$$ 비교, $$O(n)$$ 교환
- 평균 시간복잡도 : $$O(n^2)$$ 비교, $$O(n)$$ 교환  

## java 소스 구현

```java  
public class Selection {
    public static void main(String[] args) {
        int[] arr = {10, 5, 4, 1, 14, 19, 3, 13, 2, 18};
        int minIndex;
        int temp;

        for (int i = 0; i < arr.length; i++) {
            minIndex = i;

            for (int j = i + 1; j < arr.length; j++) {
                if (arr[j] < arr[minIndex]) {
                    minIndex = j;
                }
            }

            temp = arr[minIndex];
            arr[minIndex] = arr[i];
            arr[i] = temp;
        }

        //1 2 3 4 5 10 13 14 18 19
        for (int i = 0; i < arr.length; i++) {
            System.out.printf("%d ", arr[i]);
        }
    }
}
```