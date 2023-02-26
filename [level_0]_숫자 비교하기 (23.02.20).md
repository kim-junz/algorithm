# [Lv.0] 숫자 비교하기(23.02.20)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120807

#### 📌 문제 설명

정수 `num1`, `num2`가 매개변수로 주어질 때, 두 수가 같으면 1 다르면 -1을 retrun하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- 0 < num1 ≤ 10,000
- 0 < num2 ≤ 10,000

#### 📌 예시

| num1 | num2 | result |
| ---- | ---- | ------ |
| 2    | 3    | -1     |
| 11   | 11   | 1      |
| 7    | 99   | -1     |

- 입출력 예 #1
  → num1이 2이고 num2가 3이므로 다릅니다. 따라서 -1을 return합니다.

- 입출력 예 #2
  → num1이 11이고 num2가 11이므로 같습니다. 따라서 1을 return합니다.

- 입출력 예 #3
  → num1이 7이고 num2가 99이므로 다릅니다. 따라서 -1을 return합니다.

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

        answer = num1 == num2 ? 1 : -1;

        return answer;
    }
}
```

삼항연산자를 이용해 num1을 num2의 값이 같은경우에는 1을, 아닌경우에는 -1을 반환하도록 하였다.
