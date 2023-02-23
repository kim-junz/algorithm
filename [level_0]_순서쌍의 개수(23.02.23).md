# [Lv.0] 순서쌍의 개수(23.02.23)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120836

#### 📌 문제 설명

순서쌍이란 두 개의 숫자를 순서를 정하여 짝지어 나타낸 쌍으로 (a, b)로 표기합니다.  
자연수 `n`이 매개변수로 주어질 때 두 숫자의 곱이 `n`인 자연수 순서쌍의 개수를 return하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- 1 ≤ n ≤ 1,000,000

#### 📌 예시

| n   | result |
| --- | ------ |
| 20  | 6      |
| 100 | 9      |

- 입출력 예 #1
  → `n`이 20 이므로 곱이 20인 순서쌍은 (1, 20), (2, 10), (4, 5), (5, 4), (10, 2), (20, 1) 이므로 6을 return합니다.

- 입출력 예 #2
  → `n`이 100 이므로 곱이 100인 순서쌍은 (1, 100), (2, 50), (4, 25), (5, 20), (10, 10), (20, 5), (25, 4), (50, 2), (100, 1) 이므로 9를 return합니다.

#### 📌 문제

```java
class Solution {
    public int solution(int n) {
        int answer = 0;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int solution(int n) {
        int answer = 0;

        for(int i = 1; i <= n; i++ ){
            answer += n % i == 0 ? 1 : 0;
        }
        return answer;
    }
}
```

예전에 약수를 구하는 문제를 푼 적이 있다.  
i의 약수가 곧 순서쌍을 만들수 있는 숫자이므로, 약수를 구하는것과 동일하게 진행하였다  
1을 포함하여 n을 i로 나눈 값이 0일경우 answer에 1을 더하고, 0이 아닌경우 0을 더해서 증가되는 값이 없도록 하였다
