# [Lv.0] 나이 출력(23.02.20)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120820

#### 📌 문제 설명

정수 머쓱이는 40살인 선생님이 몇 년도에 태어났는지 궁금해졌습니다. 나이 `age`가 주어질 때, 2022년을 기준 출생 연도를 return 하는 solution 함수를 완성해주세요.

#### 📌 제한 조건

- 0 < age ≤ 120
- 나이는 태어난 연도에 1살이며 1년마다 1씩 증가합니다.

#### 📌 예시

| age | result |
| --- | ------ |
| 40  | 1983   |
| 23  | 2000   |

- 입출력 예 #1
  → 2022년 기준 40살이므로 1983년생입니다.

- 입출력 예 #2
  → 2022년 기준 23살이므로 2000년생입니다.

#### 📌 문제

```java
class Solution {
    public int solution(int age) {
        int answer = 0;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int solution(int age) {
        int answer = 0;

        answer = 2022 - (age-1);
        return answer;
    }
}
```

휴, 한국사람은 알수있는 1살먹고 태어나기.... 2022에서 실제 나이에서 1살을 뺀 값을 빼주었다.
