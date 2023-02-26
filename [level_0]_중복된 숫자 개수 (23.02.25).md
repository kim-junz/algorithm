# [Lv.0] 중복된 숫자 개수(23.02.25)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120583

#### 📌 문제 설명

정수가 담긴 배열 `array`와 정수 `n`이 매개변수로 주어질 때, `array`에 `n`이 몇 개 있는 지를 return 하도록 solution 함수를 완성해보세요.

#### 📌 제한 조건

- 1 ≤ array의 길이 ≤ 100
- 0 ≤ array의 원소 ≤ 1,000
- 0 ≤ n ≤ 1,000

#### 📌 예시

| array              | n   | result |
| ------------------ | --- | ------ |
| [1, 1, 2, 3, 4, 5] | 1   | 2      |
| [0, 2, 3, 4]       | 1   | 0      |

- 입출력 예 #1
  → [1, 1, 2, 3, 4, 5] 에는 1이 2개 있습니다.

- 입출력 예 #2
  → [0, 2, 3, 4] 에는 1이 0개 있습니다.

#### 📌 문제

```java
class Solution {
    public int solution(int[] array, int n) {
        int answer = 0;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int solution(int[] array, int n) {
        int answer = 0;

        for(int a : array){
            answer += a == n ? 1 : 0;
        }

        return answer;
    }
}
```

배열을 모두 검사해봐야하기 때문에 향상된 for문으로 배열의 요소와 n값을 비교하였다.
a와 n이 같을경우에는 answer에 1을 더해주었고, 일치하지 않을경우에는 0을 더해주어 일치하는 개수를 answer에 반환하도록 하였다
