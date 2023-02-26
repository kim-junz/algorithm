# [Lv.0] 나머지 구하기(23.02.20)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120810

#### 📌 문제 설명

정수 `num1`, `num2`가 매개변수로 주어질 때, `num1`를 `num2`로 나눈 나머지를 return 하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- 0 < num1 ≤ 100
- 0 < num2 ≤ 100

#### 📌 예시

| num1 | num2 | result |
| ---- | ---- | ------ |
| 3    | 2    | 1      |
| 10   | 5    | 0      |

- 입출력 예 #1
  → `num1`이 3, `num2`가 2이므로 3을 2로 나눈 나머지 1을 return 합니다.

- 입출력 예 #2
  → `num1`이 10, `num2`가 5이므로 10을 5로 나눈 나머지 0을 return 합니다.

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

        answer = num1 % num2;

        return answer;
    }
}
```

num1을 num2로 나눈 나머지값을 answer에 반환
