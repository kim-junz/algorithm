# [Lv.0] 피자 나눠 먹기(3)(23.02.24)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120816

#### 📌 문제 설명

머쓱이네 피자가게는 피자를 두 조각에서 열 조각까지 원하는 조각 수로 잘라줍니다. 피자 조각 수 slice와 피자를 먹는 사람의 수 `n`이 매개변수로 주어질 때, `n`명의 사람이 최소 한 조각 이상 피자를 먹으려면 최소 몇 판의 피자를 시켜야 하는지를 return 하도록 solution 함수를 완성해보세요.

#### 📌 제한 조건

- 2 ≤ slice ≤ 10
- 1 ≤ n ≤ 100

#### 📌 예시

| slice | n   | result |
| ----- | --- | ------ |
| 7     | 10  | 2      |
| 4     | 12  | 3      |

- 입출력 예 #1
  → 10명이 7조각으로 자른 피자를 한 조각 이상씩 먹으려면 최소 2판을 시켜야 합니다.

- 입출력 예 #2
  → 12명이 4조각으로 자른 피자를 한 조각 이상씩 먹으려면 최소 3판을 시켜야 합니다.

#### 📌 문제

```java
class Solution {
    public int solution(int slice, int n) {
        int answer = 0;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int solution(int slice, int n) {
        int answer = 0;

        answer = n % slice == 0 ? n / slice : (n / slice)+1;

        return answer;
    }
}
```

만약 slice 보다 사람이 1명이라도 초과할경우에는 1판이 추가되어야한다.  
사랑의 수를 slice 된 수로 나누었을때 0으로 나눠떨어진다면 n / slice의 몫을 그대로 반환하고,  
나눠떨어지지 않는경우에는 n/slice에서 1판을 추가한 수를 반환하도록 작성하였다
