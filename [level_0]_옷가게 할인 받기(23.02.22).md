# [Lv.0] 옷가게 할인 받기(23.02.22)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120818

#### 📌 문제 설명

머쓱이네 옷가게는 10만 원 이상 사면 5%, 30만 원 이상 사면 10%, 50만 원 이상 사면 20%를 할인해줍니다.
구매한 옷의 가격 `price`가 주어질 때, 지불해야 할 금액을 return 하도록 solution 함수를 완성해보세요.

#### 📌 제한 조건

- 10 ≤ price ≤ 1,000,000
  → price는 10원 단위로(1의 자리가 0) 주어집니다.
- 소수점 이하를 버린 정수를 return합니다.

#### 📌 예시

| price   | result  |
| ------- | ------- |
| 150,000 | 142,500 |
| 580,000 | 464,000 |

- 입출력 예 #1
  → 150,000원에서 5%를 할인한 142,500원을 return 합니다.

- 입출력 예 #2
  → 580,000원에서 20%를 할인한 464,000원을 return 합니다.

#### 📌 문제

```java
class Solution {
    public int solution(int price) {
        int answer = 0;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int solution(int price) {
        int answer = 0;

        if(price >= 100000 && price < 300000){
            answer = (int)(price * 0.95);
        }else if(price >= 300000 && price < 500000) {
            answer = (int)(price * 0.90);
        }else if (price >= 500000) {
            answer = (int)(price * 0.80);
        }else{
            answer = price;
        }
        return answer;
    }
}
```

if문을 쓴 간단한 답안이다.  
10이상~30미만은 5% 할인된 95%의 금액을 반환하도록 하고,  
30이상 ~50미만은 10% 할인된 90%의 금액을 반환하도록 하고,  
50이상은 20% 할인된 80%의 금액을 반환하도록 각 구매금액에 따라 할인된 금액을 반환해주도록 작성하였다.
