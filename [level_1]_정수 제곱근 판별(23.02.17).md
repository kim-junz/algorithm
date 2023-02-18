# [Lv.1] 정수 제곱근 판별(23.02.17)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/12934

#### 📌 문제 설명

임의의 양의 정수 n에 대해, n이 어떤 양의 정수 x의 제곱인지 아닌지 판단하려 합니다.  
n이 양의 정수 x의 제곱이라면 x+1의 제곱을 리턴하고, n이 양의 정수 x의 제곱이 아니라면 -1을 리턴하는 함수를 완성하세요.

#### 📌 제한 조건

- n은 1이상, 50000000000000 이하인 양의 정수입니다.

#### 📌 예시

| n   | return |
| --- | ------ |
| 121 | 144    |
| 3   | -1     |

#### 📌 문제

```java
class Solution {
    public long solution(long n) {
        long answer = 0;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public long solution(long n) {
        long answer = -1;

        for (long i = 0; i <= n; i++) {
            if (i * i == n) {
                answer = (i + 1) * (i + 1);
                break;
            }
        }
        return answer;
    }
}

```

n이 1일경우 1의 제곱근은 1로 1을 반환해야하므로 i는 n보다 작거나 같을때까지 for문을 돌려줘야함
그런데 이럴경우 long타입의 n이 아주 큰 숫자를 가지고있을수 있으므로 break로 맞는 제곱근 수를 찾을 경우 바로 빠져나오게 처리해야함

---

#### 💡 다른사람 풀이

```java
class Solution {
  public long solution(long n) {
      if (Math.pow((int)Math.sqrt(n), 2) == n) {
            return (long)Math.pow(Math.sqrt(n) + 1, 2);
        }

        return -1;
  }
}
```

1. `Math.pow`는 제곱근을 구하는 메서드로 `Math.pow(대상숫자,지수)`로 사용한다
   예) Math.pow(5, 2); 라고 한다면 5의 2제곱근을 반환한다.

2. `Math.sqrt`는 루트를 씌워 제곱근을 찾아내는 메서드이다.
   예) Math.sqrt(25); 라고한다면 25의 제곱근인 5를 반환한다.

위 코드를 해석해보면  
Math.pow로 찾을 제곱근은 n의 값을 모르므로, Math.sqrt(n)으로 제곱근을 찾을 숫자를 만들어주었고, 2제곱근을 찾기때문에 2를 넣어주었다  
그리고 이 값이 n과 동일할경우에 문제에서 제시한대로
Math.sqrt(n)에 1을 더한값의 제곱근을 반환하도록 하였다.

sqrt는 double타입이라 5가 들어온다면 5의 제곱근이 소숫점으로 나오므로 소숫점 이하는 버리기 위해 int로 캐스팅
