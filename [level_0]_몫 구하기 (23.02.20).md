# [Lv.0] λͺ« κ΅¬νκΈ°(23.02.20)

#### π URL : https://school.programmers.co.kr/learn/courses/30/lessons/120805

#### π λ¬Έμ  μ€λͺ

μ μ `num1`, `num2`κ° λ§€κ°λ³μ μ£Όμ΄μ§λλ€. `num1`κ³Ό `num2`λ₯Ό λλ λͺ«μ return νλλ‘ solution ν¨μλ₯Ό μμ±ν΄μ£ΌμΈμ.

#### π μ ν μ‘°κ±΄

- 0 < num1 β€ 100
- 0 < num2 β€ 100

#### π μμ

| num1 | num2 | result |
| ---- | ---- | ------ |
| 10   | 5    | 2      |
| 7    | 2    | 3      |

- μμΆλ ₯ μ #1
  β `num1`μ΄ 10, `num2`κ° 5μ΄λ―λ‘ 0μ 5λ‘ λλ λͺ« 2λ₯Ό return ν©λλ€.

- μμΆλ ₯ μ #2
  β `num1`μ΄ 7, `num2`κ° 2μ΄λ―λ‘ 7μ 2λ‘ λλ λͺ« 3μ return ν©λλ€.

#### π λ¬Έμ 

```java
class Solution {
    public int solution(int num1, int num2) {
        int answer = 0;
        return answer;
    }
}
```

---

#### βοΈ νμ΄

```java
class Solution {
    public int solution(int num1, int num2) {
        int answer = 0;

        answer = num1 / num2;
        return answer;
    }
}
```

num1μ num2λ‘ λλ κ²°κ³Όλ₯Ό answerμ λ°ν
