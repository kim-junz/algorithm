# [Lv.0] 두 수의 합(23.02.20)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120802

#### 📌 문제 설명

정수 `num1`, `num2`가 매개변수 주어집니다. `num1`과 `num2`의 합을 return하도록 soltuion 함수를 완성해주세요.

#### 📌 제한 조건

- -50000 < num1 ≤ 50000
- -50000 < num2 ≤ 50000

#### 📌 예시

| num1 | num2 | result |
| ---- | ---- | ------ |
| 2    | 3    | 5      |
| 100  | 2    | 102    |

- 입출력 예 #1
  → `num1`이 2, `num2`가 4이므로 2 + 3 = 5를 return합니다.

- 입출력 예 #2
  → `num1`이 100, `num2`가 2이므로 100 + 2 = 102를 return합니다.

#### 📌 문제

```java
class Solution {
    public int solution(int num1, int num2) {
        int answer = -1;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int solution(int num1, int num2) {
        int answer = -1;

        answer = num1 + num2;
        return answer;
    }
}
```

num1와 num2를 더한 결과를 answer에 반환
