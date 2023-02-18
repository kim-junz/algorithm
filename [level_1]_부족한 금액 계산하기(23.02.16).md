# [Lv.1] 부족한 금액 계산하기(23.02.16)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/82612

#### 📌 문제 설명

새로 생긴 놀이기구는 인기가 매우 많아 줄이 끊이질 않습니다. 이 놀이기구의 원래 이용료는 price원 인데, 놀이기구를 N 번 째 이용한다면 원래 이용료의 N배를 받기로 하였습니다. 즉, 처음 이용료가 100이었다면 2번째에는 200, 3번째에는 300으로 요금이 인상됩니다.  
놀이기구를 count번 타게 되면 현재 자신이 가지고 있는 금액에서 얼마가 모자라는지를 return 하도록 solution 함수를 완성하세요.  
단, 금액이 부족하지 않으면 0을 return 하세요.

#### 📌 제한 조건

- 놀이기구의 이용료 price : 1 ≤ price ≤ 2,500, price는 자연수
- 처음 가지고 있던 금액 money : 1 ≤ money ≤ 1,000,000,000, money는 자연수
- 놀이기구의 이용 횟수 count : 1 ≤ count ≤ 2,500, count는 자연수

#### 📌 예시

| price | money | count | result |
| ----- | ----- | ----- | ------ |
| 3     | 520   | 4     | 10     |

- 입출력 예 #1
  → 이용금액이 3인 놀이기구를 4번 타고 싶은 고객이 현재 가진 금액이 20이라면, 총 필요한 놀이기구의 이용 금액은 30(= 3+6+9+12) 이 되어 10만큼 부족하므로 10을 return 합니다.

#### 📌 문제

```java
class Solution {
    public long solution(int price, int money, int count) {
        long answer = -1;

        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public long solution(int price, long money, int count) {
        long answer = -1;
        long res = 0;

        for(int i=1; i <= count; i++){
            money -= price*i;
        }

        if(money<0){
            answer = answer*money;
        }else{
            answer = 0;
        }
            return answer;

    }
}
```

test 케이스에서 자꾸 오류가 났었는데, price값이 너무 커져서 빼다보면 money가 int의 범위를 넘어갈수 있어서 long타입으로 변경해주었다
i가 count만큼 돌면서 price의 가격을 i만큼 곱해서 money에서 빼주었다.
if문으로 money가 음수일경우에는 그만큼 부족하므로 -1이 들어있는 answer와 곱해서 반환하고,
0이상일경우에는 0으로 반환하도록 하였다

---

#### 💡 다른사람의 풀이

```java
class Solution {

    public long solution(int price, int money, int count) {

        long answer = money;

        for (int c = 0; c < count; ++c) {
            answer -= (price * (c + 1));
        }

        return (answer > 0 ? 0 : -answer);
    }
}
```

```java
class Solution {
    public long solution(int price, int money, int count) {
        long answer = -1;
        answer = (long)price*count*(count+1)/2 - money;
        return answer<=0?0:answer;
    }
}
```

마지막에 결과를 반환할때 삼항연산자를 이용해도 좋았을것 같다는 생각이 든다.
