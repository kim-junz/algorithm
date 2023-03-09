# [Lv.0] 제곱수 판별하기(23.03.01)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120909

#### 📌 문제 설명

어떤 자연수를 제곱했을 때 나오는 정수를 제곱수라고 합니다. 정수 `n`이 매개변수로 주어질 때, `n`이 제곱수라면 1을 아니라면 2를 return하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- 1 ≤ n ≤ 1,000,000

#### 📌 예시

| n   | result |
| --- | ------ |
| 144 | 1      |
| 976 | 2      |

- 입출력 예 #1
  → 144는 12의 제곱이므로 제곱수입니다. 따라서 1을 return합니다.

- 입출력 예 #2
  → 976은 제곱수가 아닙니다. 따라서 2를 return합니다.

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

        answer = n % Math.sqrt(n) == 0 ? 1 : 2;

        return answer;
    }
}
```

예전에 배워둔 Math.sqrt() 메서드다.  
해당 메서드는 매개변수에 루트를 씌워 제곱근을 찾을 수 있다.  
다만 double형으로 반환되기때문에, n을 제곱근으로 나눴을때 딱 나누어 떨어지지 않는다면 2, 나누어떨어진다면 1을 반환하도록 하였다.
