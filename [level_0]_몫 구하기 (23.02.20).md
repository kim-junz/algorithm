# [Lv.0] 몫 구하기(23.02.20)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120805

#### 📌 문제 설명

정수 `num1`, `num2`가 매개변수 주어집니다. `num1`과 `num2`를 나눈 몫을 return 하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- 0 < num1 ≤ 100
- 0 < num2 ≤ 100

#### 📌 예시

| num1 | num2 | result |
| ---- | ---- | ------ |
| 10   | 5    | 2      |
| 7    | 2    | 3      |

- 입출력 예 #1
  → `num1`이 10, `num2`가 5이므로 0을 5로 나눈 몫 2를 return 합니다.

- 입출력 예 #2
  → `num1`이 7, `num2`가 2이므로 7을 2로 나눈 몫 3을 return 합니다.

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

        answer = num1 / num2;
        return answer;
    }
}
```

num1을 num2로 나눈 결과를 answer에 반환
