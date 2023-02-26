# [Lv.0] 중앙값 구하기(23.02.25)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120811

#### 📌 문제 설명

중앙값은 어떤 주어진 값들을 크기의 순서대로 정렬했을 때 가장 중앙에 위치하는 값을 의미합니다. 예를 들어 1, 2, 7, 10, 11의 중앙값은 7입니다. 정수 배열 `array`가 매개변수로 주어질 때, 중앙값을 return 하도록 solution 함수를 완성해보세요.

#### 📌 제한 조건

- `array`의 길이는 홀수입니다.
- 0 < `array`의 길이 < 100
- -1,000 < `array`의 원소 < 1,000

#### 📌 예시

| array             | result |
| ----------------- | ------ |
| [1, 2, 7, 10, 11] | 7      |
| [9, -1, 0]        | 0      |

- 입출력 예 #1
  → 이미 오름차순으로 정렬이 되어있으며, 가운데 값인 7을 반환

- 입출력 예 #2
  → 9, -1, 0을 오름차순 정렬하면 -1, 0, 9이고 가장 중앙에 위치하는 값은 0입니다.

#### 📌 문제

```java
class Solution {
    public int solution(int[] array) {
        int answer = 0;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
import java.util.Arrays;

class Solution {
    public int solution(int[] array) {
        int answer = 0;

        Arrays.sort(array);
        answer = array[(array.length / 2)];

        return answer;
    }
}
```

배열중 가장 중간값을 반환하는 문제였다.  
이미 배열은 홀수로 되어있으므로, 짝수인 경우는 고려하지 않았다.  
sort를 사용하여 오름차순으로 정렬 후, array.length를 2로 나눈 인덱스의 array를 answer에 반환하였다  
홀수인데, 예를 들면 5/2일경우 2번째 인덱스를 반환하도록 한다.  
인덱스는 0부터 시작하기 때문에 length값을 나누기 2할경우 중앙의 인덱스값을 반환하게 된다.
