# [Lv.1] 제일 작은 수 제거하기(23.02.17)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/12935

#### 📌 문제 설명

정수를 저장한 배열, arr 에서 가장 작은 수를 제거한 배열을 리턴하는 함수, solution을 완성해주세요. 단, 리턴하려는 배열이 빈 배열인 경우엔 배열에 -1을 채워 리턴하세요. 예를들어 arr이 [4,3,2,1]인 경우는 [4,3,2]를 리턴 하고, [10]면 [-1]을 리턴 합니다.

#### 📌 제한 조건

- arr은 길이 1 이상인 배열입니다.
- 인덱스 i, j에 대해 i ≠ j이면 arr[i] ≠ arr[j] 입니다

#### 📌 예시

| arr       | return  |
| --------- | ------- |
| [4,3,2,1] | [4,3,2] |
| [10]      | [-1]    |

#### 📌 문제

```java
class Solution {
    public long solution(long n) {
        long answer = 0;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int[] solution(int[] arr) {
      int[] answer = {};

        int min = arr[0];
        int k = 0;

        if(arr.length == 1){
            answer = new int[] {-1};

        }else if(arr.length > 1) {
            answer = new int[arr.length - 1];

            for (int i = 0; i < arr.length; i++) {
                if (arr[i] < min) {
                    min = arr[i];
                }
            }
            for (int j = 0; j < arr.length; j++) {
                if (arr[j] == min){
                    continue;
                }
                answer[k++] = arr[j];
            }
        }
        return answer;
    }
}
```

먼저 for문으로 min에 arr의 0번째 값을 넣어둠  
arr의 length가 1일경우에는 바로 -1을 넣어 반환하고,  
아닐경우에는 arr에서 최소값을 뺀 배열을 복사할것이므로 arr의 length보다 1적은 answer배열을 선언함  
그다음 for문으로 돌려서 min에 넣어둔 arr값과 하나씩 비교하여 min이 더 클경우에는 해당 arr의 i번째값을 min에 넣어 최소값을 찾아  
최소값을 min에 저장해둠

answer의 index값으로 사용될k를 0으로 선언하였고  
for문으로 생성해둔 answer[k]에 arr의 값을 한개씩 복사해서 넣는데, 그중 arr의 j번째 값이 min값과 동일할경우는 그냥 지나침  
for문으로 k++하여 차례대로 arr[j]의 값을 넣어줌  
복사성공

`그리고 또 다른 풀이 ㅠㅠ`

```java
class Solution {
    public int[] solution(int[] arr) {
      int[] answer = {};

        int min = arr[0];
        int k = 0;
        int index = 0;

        if(arr.length == 1){
            answer = new int[] {-1};

        }else if(arr.length > 1) {
            answer = new int[arr.length - 1];

            for (int i = 0; i < arr.length; i++) {
                if (arr[i] < min) {
                    min =arr[i]; //min을 저장하지 않아서 min이 계속 [0]값이었기 때문...
                    index = i;
                }
            }
            for (int j = 0; j < arr.length; j++) {
                if ( j == index) {

                    continue;
                }
                answer[k++] = arr[j];
            }
        }
        return answer;
    }
}
```

원래 풀었던건 이 코드였는데, 저 주석이 달린 부분을 빼먹어서 자꾸 원하는 답이 나오지 않았다.  
그래서 위에 먼저 올렸던 코드로 채점을 진행했다 ㅠㅠ  
index값으로 위치를 비교한다고 index만 저장해주었다; min값을 저장해주지 않으니까 저 for문에서 제대로 최소값을 저장해주지 않았기 때문에 i가 최소값의 index위치를 반환하지 않았던것.

위와 같이 빠진 코드를 추가한 후 j와 index를 비교하여 arr의 해당 index위치의 요소를 빼고 배열을 복사해도 된다
