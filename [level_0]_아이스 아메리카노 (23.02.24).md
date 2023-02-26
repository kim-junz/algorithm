# [Lv.0] 아이스 아메리카노(23.02.24)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120819

#### 📌 문제 설명

머쓱이는 추운 날에도 아이스 아메리카노만 마십니다. 아이스 아메리카노는 한잔에 5,500원입니다. 머쓱이가 가지고 있는 돈 `money`가 매개변수로 주어질 때, 머쓱이가 최대로 마실 수 있는 아메리카노의 잔 수와 남는 돈을 순서대로 담은 배열을 return 하도록 solution 함수를 완성해보세요.

#### 📌 제한 조건

- 0 < money ≤ 1,000,000

#### 📌 예시

| money  | result    |
| ------ | --------- |
| 5,500  | [1, 0]    |
| 15,000 | [2, 4000] |

- 입출력 예 #1
  → 5,500원은 아이스 아메리카노 한 잔을 살 수 있고 잔돈은 0원입니다.

- 입출력 예 #2
  → 15,000원은 아이스 아메리카노 두 잔을 살 수 있고 잔돈은 4,000원입니다.

#### 📌 문제

```java
class Solution {
    public int[] solution(int money) {
        int[] answer = {};
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int[] solution(int money) {
        int[] answer = new int[2];

        answer[0] = money / 5500;
        answer[1] = money % 5500;

        return answer;
    }
}
```

배열 answer에는 총 몇잔인지, 그리고 남은돈은 얼마인지 반환하도록 되어있기때문에,  
answer에는 데이터가 2개가 들어갈 수 있는 배열을 생성해두었고,  
answer[0]번째 인덱스에는 5500원짜리 아메리카노를 몇개를 살수 있는지 money를 5500으로 나눈 몫,  
answer[1]번째 인덱스에는 money를 5500으로 나눈 나머지를 넣어주었다.
