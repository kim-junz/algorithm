# [Lv.0] 짝수는 싫어요(23.02.25)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120813

#### 📌 문제 설명

정수 `n`이 매개변수로 주어질 때, `n` 이하의 홀수가 오름차순으로 담긴 배열을 return하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- 1 ≤ n ≤ 100

#### 📌 예시

| n   | result                      |
| --- | --------------------------- |
| 10  | [1, 3, 5, 7, 9]             |
| 15  | [1, 3, 5, 7, 9, 11, 13, 15] |

- 입출력 예 #1
  → 10 이하의 홀수가 담긴 배열 [1, 3, 5, 7, 9]를 return합니다.

- 입출력 예 #2
  → 15 이하의 홀수가 담긴 배열 [1, 3, 5, 7, 9, 11, 13, 15]를 return합니다.

#### 📌 문제

```java
class Solution {
    public int[] solution(int n) {
        int[] answer = {};
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int[] solution(int n) {
        int[] answer = new int[n%2 == 0 ? n/2 : (n/2)+1];
        int j = 0;

        for(int i=1; i <= n; i++){
           if(i % 2 != 0){
               answer[j] = i;
               j++;
            }
        }

        return answer;
    }
}
```

answer의 배열의 크기는 n이 짝수일경우 n을 2로 나눈 값, 짝수가 아닐경우는 n을 2로 나눈것에 +1만큼의 크기가 필요하여 삼항연산자를 통하여 크기를 정해주었다  
for문으로 n을 1부터 n까지 1씩 증가시켜서 홀수여부를 판단하여 answer에 넣어주어야하는데,
값이 들어올경우 다음 인덱스로 넘어가야하기 때문에, int j를 선언하여 0으로 초기화 해준 뒤, answer의 인덱스값으로 사용하였다.

---

#### 💡 다른사람의 풀이

```java
import java.util.*;

class Solution {
    public ArrayList solution(int n) {
        ArrayList<Integer> answer = new ArrayList<Integer>();

        for(int i=1; i<=n; i++){
          if(i%2 != 0) {
              answer.add(i);
          }
        }

        return answer;
    }
}
```

처음에 ArrayList로 작성해주고자 하였는데, 공부가 부족해서 사용법을 몰라서 그랬을까 ㅠㅠ 실패하였었다.
풀이를 보니 내가 사용하고싶었던 코드로 작성하신분이 계셔서 코드를 가져와보았다.
앞으로는 써먹을수 있도록 해야겠다.
