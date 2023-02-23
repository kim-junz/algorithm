# [Lv.0] 배열 두배 만들기(23.02.23)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120809

#### 📌 문제 설명

정수 배열 `numbers`가 매개변수로 주어집니다. `numbers`의 각 원소에 두배한 원소를 가진 배열을 return하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- 10,000 ≤ numbers의 원소 ≤ 10,000
- 1 ≤ numbers의 길이 ≤ 1,000

#### 📌 예시

| numbers                   | result                     |
| ------------------------- | -------------------------- |
| [1, 2, 3, 4, 5]           | [2, 4, 6, 8, 10]           |
| [1, 2, 100, -99, 1, 2, 3] | [2, 4, 200, -198, 2, 4, 6] |

- 입출력 예 #1
  → [1, 2, 3, 4, 5]의 각 원소에 두배를 한 배열 [2, 4, 6, 8, 10]을 return합니다.

- 입출력 예 #2
  → [1, 2, 100, -99, 1, 2, 3]의 각 원소에 두배를 한 배열 [2, 4, 200, -198, 2, 4, 6]을 return합니다.

#### 📌 문제

```java
class Solution {
    public int[] solution(int[] numbers) {
        int[] answer = {};
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int[] solution(int[] numbers) {
        int[] answer = new int[numbers.length];

        for(int i=0; i < numbers.length; i++){
            answer[i] = numbers[i]*2;
        }

        return answer;
    }
}
```

numbers의 배열 요소를 \*2를 하여 answer의 배열에 차례대로 넣어주었다.
