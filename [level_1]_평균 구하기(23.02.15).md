# [Lv.1] 평균 구하기(23.02.15)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/12944

#### 📌 문제 설명

정수를 담고 있는 배열 arr의 평균값을 return하는 함수, solution을 완성해보세요.

#### 📌 제한 조건

- arr은 길이 1 이상, 100 이하인 배열입니다.
- arr의 원소는 -10,000 이상 10,000 이하인 정수입니다.

#### 📌 예시

| arr       | return |
| --------- | ------ |
| [1,2,3,4] | 2.5    |
| [5,5]     | 5      |

#### 📌 문제

```java
class Solution {
    public double solution(int[] arr) {
        double answer = 0;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public double solution(int[] arr) {
        double answer = 0;
        double sum = 0;

        for(int a : arr){
            sum += a;
        }
        answer = sum / arr.length;

        return answer;
    }
}

```

배열 arr을 for문으로 double 타입의 sum에 더해주고, 해당 sum을 arr의 길이만큼 나누어줌  
sum값이 실수가 나올수도 있으므로 double 타입으로 선언해준것  
