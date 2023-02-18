# [Lv.1] 없는 숫자 더하기

#### 📌 날짜 : 2023.02.15

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/86051

#### 📌 문제 설명

0부터 9까지의 숫자 중 일부가 들어있는 정수 배열 numbers가 매개변수로 주어집니다. numbers에서 찾을 수 없는 0부터 9까지의 숫자를 모두 찾아
더한 수를 return 하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- 1 ≤ `numbers`의 길이 ≤ 9
  - 0 ≤ `numbers`의 모든 원소 ≤ 9
  - `numbers`의 모든 원소는 서로 다릅니다.

#### 📌 예시

| numbers           | result |
| ----------------- | ------ |
| [1,2,3,4,6,7,8,0] | 14     |
| [5,8,4,0,6,7,9]   | 6      |

- 입출력 예 #1
  → 5, 9가 numbers에 없으므로, 5 + 9 = 14를 return 해야 합니다.

- 입출력 예 #2
  → 1, 2, 3이 numbers에 없으므로, 1 + 2 + 3 = 6을 return 해야 합니다.

#### 📌 문제

```java
class Solution {
    public int solution(int[] numbers) {
        int answer = -1;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int solution(int[] numbers) {
        int answer = 0;
        int count =0;

        for(int i = 0; i<=9; i++){
            count += i;
        }

        for(int a : numbers) {
            answer = count -=a;
        }

        return answer;
    }
}

```

0부터 9까지의 숫자 합에서, 배열의 숫자 합을 빼주었다  
이런 방식이 아니고, 다른 방식이 있는거같은데 스트림써야한다고해서 일단 내 레벨은 아닌것같아 이정도로 진행하였다
