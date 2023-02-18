# [Lv.1] 나누어 떨어지는 숫자 배열(23.02.16)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/12910

#### 📌 문제 설명

array의 각 element 중 divisor로 나누어 떨어지는 값을 오름차순으로 정렬한 배열을 반환하는 함수, solution을 작성해주세요.  
divisor로 나누어 떨어지는 element가 하나도 없다면 배열에 -1을 담아 반환하세요.

#### 📌 제한 조건

- arr은 자연수를 담은 배열입니다.
- 정수 i, j에 대해 i ≠ j 이면 arr[i] ≠ arr[j] 입니다.
- divisor는 자연수입니다.
- array는 길이 1 이상인 배열입니다.

#### 📌 예시

| arr           | divisor | return        |
| ------------- | ------- | ------------- |
| [5, 9, 7, 10] | 5       | [5, 10]       |
| [2, 36, 1, 3] | 1       | [1, 2, 3, 36] |
| [3,2,6]       | 10      | [-1]          |

- 입출력 예 #1
  → 1arr의 원소 중 5로 나누어 떨어지는 원소는 5와 10입니다. 따라서 [5, 10]을 리턴합니다.
- 입출력 예 #2
  → 2arr의 모든 원소는 1으로 나누어 떨어집니다. 원소를 오름차순으로 정렬해 [1, 2, 3, 36]을 리턴합니다.
- 입출력 예 #3
  → 33, 2, 6은 10으로 나누어 떨어지지 않습니다. 나누어 떨어지는 원소가 없으므로 [-1]을 리턴합니다.

#### 📌 문제

```java
class Solution {
    public int[] solution(int[] arr, int divisor) {
        int[] answer = {};
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
import java.util.Arrays;
class Solution {
    public int[] solution(int[] arr, int divisor) {
         int[] answer = {};
        int i = 0;
        int j = 0;

        for (int a : arr) {
            if (a % divisor == 0) {
                i++;
            }
        }

        if (i == 0) {
            answer = new int[]{-1};
        } else {
            answer = new int[i];
            for (int b : arr) {
                if (b % divisor == 0) {
                    answer[j] = b;
                    j++;
                }
            }
            Arrays.sort(answer);
        }
        return answer;
    }
}
```

문제가 개편되어서 다른 사람들의 코드를 볼수 없는게 아쉽다 ㅠ  
먼저 첫번째 for문으로 딱 나누어떨어지는 숫자가 몇개있는지 확인하고 만약 없을경우에는 -1을 반환,  
있을경우에는 해당 크기만큼 배열을 생성해주어서 맞아떨어지는 배열을 answer에 넣었다.  
마지막에 오름차순 정렬해주고 return...  
좀더 효율적인 방법이 있을것같기도 한데, 아직은 모르겠다. 나중에 또 풀어게 되면 지금이랑 다를까?  
지금알수없지만 그때 비교해보면 좋을것같다
