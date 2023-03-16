# [Lv.0] 최댓값 만들기 (2)(23.03.06)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120862

#### 📌 문제 설명

정수 배열 `numbers`가 매개변수로 주어집니다. `numbers`의 원소 중 두 개를 곱해 만들 수 있는 최댓값을 return하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- -10,000 ≤ `numbers`의 원소 ≤ 10,000
- 2 ≤ `numbers` 의 길이 ≤ 100

#### 📌 예시

| numbers                   | result |
| ------------------------- | ------ |
| [1, 2, -3, 4, -5]         | 15     |
| [0, -31, 24, 10, 1, 9]    | 240    |
| [10, 20, 30, 5, 5, 20, 5] | 600    |

- 입출력 예 #1
  → 두 수의 곱중 최댓값은 -3 \* -5 = 15 입니다.

- 입출력 예 #2
  → 두 수의 곱중 최댓값은 10 \* 24 = 240 입니다.

- 입출력 예 #3
  → 두 수의 곱중 최댓값은 20 \* 30 = 600 입니다.

#### 📌 문제

```java
class Solution {
    public int solution(int[] numbers) {
        int answer = 0;
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

        if(numbers.length == 2 ){
            answer = numbers[0] * numbers[1];
        }
        for(int i=0; i<numbers.length; i++){
           for(int j = 0; j<numbers.length; j++){
               if(i != j){
                    answer = Math.max(answer, numbers[j] * numbers[i]);
               }
           }
        }
        return answer;
    }
}
```

원래 for문만 작성하였는데, 테스트 7번에서 통과를 못하였다.  
질문하기에서 확인해보니, 배열에 딱 2개의 요소만 있을때 두개의 곱이 -일경우 answer가 0이면 0을 반환하기 때문...  
그래서 if로 배열이 2개일경우에는 해당 요소의 곱을 반환하고, 그 외에는 자기 자신의 인덱스 외 다른 인덱스들을 곱했을때 더 큰 숫자를 반환하도록 하였다

---

#### 💡 다른사람의 풀이

```java
class Solution {
    public int solution(int[] numbers) {
        int answer = Integer.MIN_VALUE;
        for(int i = 0; i < numbers.length; i++){
            for(int j = i + 1; j < numbers.length; j++){
                answer = Math.max(answer, numbers[i] * numbers[j]);
            }
        }
        return answer;
    }
}
```

나와 같은 풀이지만 answer를 다르게 지정한경우가 있어서 가져왔다.
integer의 가장 최소값을 answer에 넣을 경우, 두 요소의 최대값이 -이더라도 해결되기 때문에 좋은 방법인것 같다.

```java
import java.util.*;

class Solution {
    public int solution(int[] numbers) {
        int len = numbers.length;
        Arrays.sort(numbers);
        return Math.max(numbers[0] * numbers[1], numbers[len - 2] * numbers[len - 1]);
    }
}
```

먼저 배열을 sort해 줄 경우, 오름차순으로 정렬된다
만약 {-10, -20, 3, 5, 20, 50}으로 정렬될경우
맨 앞의 두개의 요소 곱과 맨 뒤의 두개의 요소 곱 중 더 큰 수를 return하는것이다.
ㅠㅠ나는 언제쯤 저렇게 똑똑해질 수 있을까....................
