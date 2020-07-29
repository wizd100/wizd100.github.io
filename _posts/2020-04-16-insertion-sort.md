---
title:  "삽입정렬(Insertion sort) 소스코드"
tags: [정렬, 알고리즘, java]
use_math: true
comments: true
read_time: false
---

<iframe src="https://www.youtube.com/embed/ROalU379l3U" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## 삽입정렬이란?
자료 배열의 모든 요소를 앞에서부터 차례대로 이미 정렬된 배열 부분과 비교하여,<br>
자신의 위치를 찾아 삽입함으로써 정렬을 완성하는 알고리즘

    5 3 6 1 4 - 시작
    3 5 6 1 4 - 5와 3 비교하여 교환 1 pass
    3 5 6 1 4 - 5와 6을 비교하고 2 pass
    3 5 1 6 4 - 6과 1을 비교하고 교환
    3 1 5 6 4 - 정렬된 5와 1를 비교하고 교환
    1 3 5 6 4 - 정렬된 3과 1를 비교하고 교환 3 pass
    1 3 5 4 6 - 6과 4를 비교하고 교환
    1 3 4 5 6 - 정렬된 5와 4를 비교하고 교환
    1 3 4 5 6 - 정렬된 3과 4를 비교하고 정렬 완료
    
##삽입정렬 특징
- 장점
    1. 구현이 간단하다
        * 버블정렬, 선택정렬 알고리즘보다 빠르다
    2. 안정 정렬이다
- 단점
    1. 배열이 길어질수록 효율이 떨어진다
    
## 시간복잡도
- 최악 시간복잡도 : $$O(n^2)$$ 비교, $$O(n^2)$$ 교환
- 최선 시간복잡도 : $$O(n)$$ 비교, $$O(1)$$ 교환
- 평균 시간복잡도 : $$O(n^2)$$ 비교, $$O(n^2)$$ 교환

## java 소스 구현

```java  
public class Insertion {
    public static void main(String[] args) {
        int[] arr = {10, 3, 5, 1, 7, 6, 9, 2, 4, 8};
        int temp;
        int sortedIndex;
        /*
        * 10 3 5 1 7 6 9 2 4 8 - 시작
        * 3 10| 5 1 7 6 9 2 4 8 - 첫번째 패스
        * 3 5 10| 1 7 6 9 2 4 8 - 두번째 패스
        * 3 5 1 10| 7 6 9 2 4 8 - 교환 10 1
        * 3 1 5 10| 7 6 9 2 4 8 - 교환 5 1
        * 1 3 5 10| 7 6 9 2 4 8 - 교환 3 1 세번째 패스
        * */

        for (int i = 0; i < arr.length - 1; i++) {
            sortedIndex = i + 1;
            //정렬이 안된 값을 교환
            if (arr[i] > arr[i + 1]) {
                temp = arr[i];
                arr[i] = arr[i + 1];
                arr[i + 1] = temp;
            }

            //이미 정렬이 된 값을 교환
            for (int j = sortedIndex; j > 0; j--) {
                if (arr[j - 1] > arr[j]) {
                    temp = arr[j];
                    arr[j] = arr[j - 1];
                    arr[j - 1] = temp;
                }
            }
        }

        for (int i = 0; i < arr.length; i++) {
            System.out.printf("%d ", arr[i]);
        }
    }
}
```