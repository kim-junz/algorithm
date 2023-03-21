# [Lv.0] 가장 큰 수 찾기(23.03.07)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120899

#### 📌 문제 설명

정수 배열 `array`가 매개변수로 주어질 때, 가장 큰 수와 그 수의 인덱스를 담은 배열을 return 하도록 solution 함수를 완성해보세요.

#### 📌 제한 조건

- 1 ≤ `array`의 길이 ≤ 100
- 0 ≤ `array` 원소 ≤ 1,000
- `array`에 중복된 숫자는 없습니다.

#### 📌 예시

| array          | result  |
| -------------- | ------- |
| [1, 8, 3]      | [8, 1]  |
| [9, 10, 11, 8] | [11, 2] |

- 입출력 예 #1
  → 1, 8, 3 중 가장 큰 수는 8이고 인덱스 1에 있습니다.

- 입출력 예 #2
  → 9, 10, 11, 8 중 가장 큰 수는 11이고 인덱스 2에 있습니다.

#### 📌 문제

```java
class Solution {
    public int[] solution(int[] array) {
        int[] answer = {};
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int[] solution(int[] array) {
        int[] answer = new int[2];
        answer[0] = 0;

        for(int i=0; i< array.length; i++){
            if(answer[0] < array[i]){
                answer[0] = array[i];
                answer[1] = i;
            }
        }
        return answer;
    }
}
```

answer의 0번째 인덱스에는 array의 max값, answer의 1번째 인덱스에는 array max값의 index를 반환하므로, 변수를 따로 선언하지않고   
바로 answer[0]과 answer[1]을 활용하였음   
answer[0]을 0으로 초기화 하고 for문으로 array의 인덱스값을 하나씩 꺼내서 비교하여 answer[0]보다 클 경우에 answer[0]에 대입하고, 
해당 i값을 answer[1]에 저장하도록 하였다   
