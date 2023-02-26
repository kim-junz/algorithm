# [Lv.0] 피자 나눠 먹기 (1)(23.02.20)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120814

#### 📌 문제 설명

머쓱이네 피자가게는 피자를 일곱 조각으로 잘라 줍니다. 피자를 나눠먹을 사람의 수 `n`이 주어질 때, 모든 사람이 피자를 한 조각 이상 먹기 위해 필요한 피자의 수를 return 하는 solution 함수를 완성해보세요.

#### 📌 제한 조건

- 1 ≤ `n` ≤ 100

#### 📌 예시

| n   | result |
| --- | ------ |
| 7   | 1      |
| 1   | 1      |
| 15  | 3      |

- 입출력 예 #1
  → 7명이 최소 한 조각씩 먹기 위해서 최소 1판이 필요합니다.

- 입출력 예 #2
  → 1명은 최소 한 조각을 먹기 위해 1판이 필요합니다.

  - 입출력 예 #3
    → 15명이 최소 한 조각씩 먹기 위해서 최소 3판이 필요합니다.

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
        int answer = n % 7 == 0 ? n / 7 : (n / 7)+1;

        return answer;
    }
}
```

사람 수가 7조각보다 초과하면 무조건 한판이 더 필요하기때문에,  
n % 7 이 0일경우에는 n / 7의 몫을 그대로 반환하고, 아닐경우에는 n / 7의 몫에 1을 더하여 반환하였음
