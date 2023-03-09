# [Lv.0] 최빈값 구하기(23.02.28)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120812

#### 📌 문제 설명

최빈값은 주어진 값 중에서 가장 자주 나오는 값을 의미합니다. 정수 배열 `array`가 매개변수로 주어질 때, 최빈값을 return 하도록 solution 함수를 완성해보세요. 최빈값이 여러 개면 -1을 return 합니다.

#### 📌 제한 조건

- 0 < array의 길이 < 100
- 0 ≤ array의 원소 < 1000

#### 📌 예시

| denom2             | result |
| ------------------ | ------ |
| [1, 2, 3, 3, 3, 4] | 3      |
| [1, 1, 2, 2]       | -1     |
| [1]                | 1      |

- 입출력 예 #1
  → [1, 2, 3, 3, 3, 4]에서 1은 1개 2는 1개 3은 3개 4는 1개로 최빈값은 3입니다.

- 입출력 예 #2
  → [1, 1, 2, 2]에서 1은 2개 2는 2개로 최빈값이 1, 2입니다. 최빈값이 여러 개이므로 -1을 return 합니다.

- 입출력 예 #3  
  → [1]에는 1만 있으므로 최빈값은 1입니다.

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
        int max= 0;

        Arrays.sort(array);

        for(int i=0; i < array.length; i++){
            int cnt = 0;
           for(int j = 0; j < array.length; j++){
               if(array[j] == array[i]){
                   cnt++;
               }
           }
           if(cnt > max){
               max = cnt;
               answer = array[i];
           }else if (cnt == max && array[i] != answer){
               answer = -1;
           }
        }

        return answer;
    }
}
```

일단 배열을 sort하여 정렬해준다  
가장 많이 나오는 배열 값을 몇번 나왔는지 저장할만한 max를 선언하여 0으로 초기화 해둔다

for문으로 array의 i번째 인덱스 값과 j번째 인덱스 값을 비교하여 동일할경우에는 cnt를 1씩 증가시키고,  
아닐경우에는 빠져나와서 cnt를 0으로 초기화한다

이따 cnt값이 max값보다 클 경우에는 max에 cnt값을 넣고 answer에 array[i]값을 넣어준다. 클 경우니까 가장 큰 순간의 array값을 넣어주는것임  
그리고 만약 cnt와 max가 동일하고, array의 i번째 값이 answer와 같지 않을경우에 → 즉 최빈값과 똑같은 cnt값이 또 있는 경우에는 answer에 -1을 반환...

이건 좀 많이 어려웠다 ㅠㅠㅠ 풀고나니 +7점........
