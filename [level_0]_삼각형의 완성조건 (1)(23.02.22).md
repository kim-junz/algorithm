# [Lv.0] 삼각형의 완성조건 (1)(23.02.22)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120889

#### 📌 문제 설명

선분 세 개로 삼각형을 만들기 위해서는 다음과 같은 조건을 만족해야 합니다.

- 가장 긴 변의 길이는 다른 두 변의 길이의 합보다 작아야 합니다.  
  삼각형의 세 변의 길이가 담긴 배열 sides이 매개변수로 주어집니다. 세 변으로 삼각형을 만들 수 있다면 1, 만들 수 없다면 2를 return하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- `sides`의 원소는 자연수입니다.
- `sides`의 길이는 3입니다.
- 1 ≤ `sides`의 원소 ≤ 1,000

#### 📌 예시

| sides          | result |
| -------------- | ------ |
| [1, 2, 3]      | 2      |
| [3, 6, 2]      | 2      |
| [199, 72, 222] | 1      |

- 입출력 예 #1
  → 가장 큰 변인 3이 나머지 두 변의 합 3과 같으므로 삼각형을 완성할 수 없습니다. 따라서 2를 return합니다.

- 입출력 예 #2
  → 가장 큰 변인 6이 나머지 두 변의 합 5보다 크므로 삼각형을 완성할 수 없습니다. 따라서 2를 return합니다.

- 입출력 예 #3
  → 가장 큰 변인 222가 나머지 두 변의 합 271보다 작으므로 삼각형을 완성할 수 있습니다. 따라서 1을 return합니다.

#### 📌 문제

```java
class Solution {
    public int solution(int[] sides) {
        int answer = 0;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int solution(int[] sides) {
        int answer = 0;
        int max = sides[0];
        int res = 0;

        for(int i =0; i < sides.length; i++){
            if(max < sides[i]){
                max = sides[i];
            }
            res += sides[i];
        }
        res -= max;

       answer = max >= res ? 2 : 1;
        return answer;
    }
}
```

max를 선언하고 sides[0]로 초기화 한 다음, for문으로 sides의 배열 중 가장 큰 숫자를 찾아 저장하고,  
res에는 sides의 값을 저장 후 max의 값만큼 빼주었다.

max에 든 값이 res보다 크거나 같으면 2를, 그렇지 않으면 1을 반환하도록 하였다

---

#### 💡 다른사람의 풀이

```java
import java.util.Arrays;
class Solution {
    public int solution(int[] sides) {
        int answer = 0;
        Arrays.sort(sides);
        return sides[2] >= sides[0]+sides[1] ? 2 : 1;
    }
}
```

가장 큰 값을 찾기 위해 sort를 해주어 가장 마지막인 2번째 인덱스의 값과 나머지 0번째, 1번째 인덱스의 합을 비교하여  
2번째 값이 더 크거나 같으면 2, 그렇지 않으면 1을 반환하도록 3항연산자를 사용하였다  
코드가 간결하고 sort로 max값을 찾은것이 좋은것같다. 배열의 순서가 바뀌면 안된다는 말은 없었다
