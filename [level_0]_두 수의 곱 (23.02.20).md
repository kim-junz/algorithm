# [Lv.0] 두 수의 곱(23.02.20)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120804

#### 📌 문제 설명

정수 `num1`, `num2`가 매개변수 주어집니다. `num1`과 `num2`를 곱한 값을 return 하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- 0 < num1 ≤ 100
- 0 < num2 ≤ 100

#### 📌 예시

| num1 | num2 | result |
| ---- | ---- | ------ |
| 3    | 4    | 12     |
| 27   | 19   | 513    |

- 입출력 예 #1
  → `num1`이 3, `num2`가 4이므로 3 \* 4 = 12를 return합니다.

- 입출력 예 #2
  → `num1`이 27, `num2`가 19이므로 27 \* 19 = 513을 return합니다.

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
    public int solution(int num1, int num2) {
        int answer = 0;

        answer = num1 * num2;
        return answer;
    }
}
```

num1을 num2로 곱한 결과를 answer에 반환
