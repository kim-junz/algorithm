# [Lv.0] 약수 구하기(23.03.09)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120897

#### 📌 문제 설명

정수 `n`이 매개변수로 주어질 때, `n`의 약수를 오름차순으로 담은 배열을 return하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- 1 ≤ `n` ≤ 10,000

#### 📌 예시

| n   | result                     |
| --- | -------------------------- |
| 24  | [1, 2, 3, 4, 6, 8, 12, 24] |
| 29  | [1, 29]                    |

- 입출력 예 #1
  → 24의 약수를 오름차순으로 담은 배열 [1, 2, 3, 4, 6, 8, 12, 24]를 return합니다.

- 입출력 예 #2
  → 29의 약수를 오름차순으로 담은 배열 [1, 29]를 return합니다.

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
        int count = 0;
        int j = 0;
        
        for(int i = 1; i <= n; i++){
            count += n % i == 0 ? 1 : 0;
        }

        int[] answer = new int[count];

        for(int i = 1; i <= n; i++){
            if(n % i == 0){
                answer[j] = i;
                j++;
            }
        }
        return answer;
    }
}
```

나도 격하게 ArrayList쓰고싶다.... 그럼 코드가 많이 줄어들텐데 ㅠㅠ.. 왜 통과가 안되는지 모르겠네 IDE에서는 문제없었음...   
일단 for문으로 1부터시작하여 n이 0으로 나눠떨어지는 경우의 수가 몇개인지 확인 후 count에 넣어줌   
그리고 해당 count의 값으로 answer의 배열의 크기를 지정해주고,   
다시 for문을 통해서 0으로 나눠떨어지게 하는 i를 answer의 배열에 넣어준다   