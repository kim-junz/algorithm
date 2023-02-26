# [Lv.0] 두 수의 나눗셈(23.02.20)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120803

#### 📌 문제 설명

정수 `num1`, `num2`가 매개변수 주어집니다. `num1`를 `num2`로 나눈 값에 1,000을 곱한 후 정수 부분을 return 하도록 soltuion 함수를 완성해주세요.

#### 📌 제한 조건

- 0 < num1 ≤ 100
- 0 < num2 ≤ 100

#### 📌 예시

| num1 | num2 | result |
| ---- | ---- | ------ |
| 3    | 2    | 1500   |
| 7    | 3    | 2333   |
| 1    | 16   | 62     |

- 입출력 예 #1
  → num1이 3, num2가 2이므로 3 / 2 = 1.5에 1,000을 곱하면 1500이 됩니다.

- 입출력 예 #2
  → num1이 7, num2가 3이므로 7 / 3 = 2.33333...에 1,000을 곱하면 2333.3333.... 이 되며, 정수 부분은 2333입니다.

  - 입출력 예 #3
    → num1이 1, num2가 16이므로 1 / 16 = 0.0625에 1,000을 곱하면 62.5가 되며, 정수 부분은 62입니다.

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
        double res = 0;

        res= (double)num1/num2;
        answer = (int)(res*1000);

        return answer;
    }
}
```

나눈 몫의 값은 int로 반환되기 때문에 소숫점 아래가 표시되지 않는다.  
double로 형변환을 해줄 경우 소숫점 아래 몫의 값도 표시가 되고, 이 나눈 값에 1000을 곱해주었다.
