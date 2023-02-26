# [Lv.0] 최댓값 만들기 (1)(23.02.24)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120847

#### 📌 문제 설명

정수 배열 `numbers`가 매개변수로 주어집니다. `numbers`의 원소 중 두 개를 곱해 만들 수 있는 최댓값을 return하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- 0 ≤ numbers의 원소 ≤ 10,000
- 2 ≤ numbers의 길이 ≤ 100

#### 📌 예시

| numbers               | result |
| --------------------- | ------ |
| [1, 2, 3, 4, 5]       | 20     |
| [0, 31, 24, 10, 1, 9] | 744    |

- 입출력 예 #1
  → 두 수의 곱중 최댓값은 4 \* 5 = 20 입니다.

- 입출력 예 #2
  → 두 수의 곱중 최댓값은 31 \* 24 = 744 입니다.

#### 📌 문제

```java
class Solution {
    public int solution(int[] numbers) {
        int answer = 0;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
import java.util.Arrays;

class Solution {
    public int solution(int[] numbers) {
        int answer = 0;

        Arrays.sort(numbers);

        answer = numbers[numbers.length - 1] * numbers[numbers.length - 2];

        return answer;
    }
}
```

가장 큰 수 두개의 위치가 뒤죽박죽이기 때문에, 먼저 sort로 오름차순으로 정리하였다.
그리고 answer에는 numbers의 마지막인덱스와, 두번째 마지막 인덱스를 곱해주었다
