# [Lv.0] 짝수의 합(23.02.20)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120831

#### 📌 문제 설명

정수 `n`이 주어질 때, `n`이하의 짝수를 모두 더한 값을 return 하도록 solution 함수를 작성해주세요.

#### 📌 제한 조건

- 0 < n ≤ 1000

#### 📌 예시

| n   | result |
| --- | ------ |
| 10  | 30     |
| 4   | 6      |

- 입출력 예 #1
  → n이 10이므로 2 + 4 + 6 + 8 + 10 = 30을 return 합니다.

- 입출력 예 #2
  → n이 4이므로 2 + 4 = 6을 return 합니다.

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
        int answer = 0;

        for(int i = 2; i <= n; i++){
            answer += i % 2 == 0 ? i : 0;
        }
        return answer;
    }
}
```

for문으로 어차피 짝수부터 찾는거라면 i를 0부터 시작이 아닌, 2부터 시작하여 int i를 1씩 증가시키면서  
2를 포함하여 짝수일경우에는 해당 i를 answer에 더하고, 홀수인경우는 0을 더해주어 반환하였다.
