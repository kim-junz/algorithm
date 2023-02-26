# [Lv.0] 배열의 평균값(23.02.20)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120817

#### 📌 문제 설명

정수 배열 `numbers`가 매개변수로 주어집니다. `numbers`의 원소의 평균값을 return하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- 0 ≤ `numbers`의 원소 ≤ 1,000
- 1 ≤ `numbers`의 길이 ≤ 100
- 정답의 소수 부분이 .0 또는 .5인 경우만 입력으로 주어집니다.

#### 📌 예시

| numbers                                      | result |
| -------------------------------------------- | ------ |
| [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]              | 5.5    |
| [89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99] | 94.0   |

- 입출력 예 #1
  → numbers의 원소들의 평균 값은 5.5입니다.

- 입출력 예 #2
  → numbers의 원소들의 평균 값은 94.0입니다.

#### 📌 문제

```java
class Solution {
    public int solution(int num1, int num2) {
        int answer = 0;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public double solution(int[] numbers) {
        double answer = 0;
        double count = 0;

          for(int a : numbers ){
             count += a;
          }
            answer = count / numbers.length;

        return answer;
    }
}
```

numbers 배열에 있는 값을 count에 더해주었다.  
count를 numbers.length만큼 나누어주고, 나눠준 값이 소숫점이 나올 수 있으므로,  
count를 double로 선언하였다.
