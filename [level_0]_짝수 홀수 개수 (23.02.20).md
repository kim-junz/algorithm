# [Lv.0] 짝수 홀수 개수(23.02.20)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120824

#### 📌 문제 설명

정수가 담긴 리스트 `num_list`가 주어질 때, `num_list`의 원소 중 짝수와 홀수의 개수를 담은 배열을 return 하도록 solution 함수를 완성해보세요.

#### 📌 제한 조건

- 1 ≤ `num_list`의 길이 ≤ 100
- 0 ≤ `num_list`의 원소 ≤ 1,000

#### 📌 예시

| num_list        | result |
| --------------- | ------ |
| [1, 2, 3, 4, 5] | [2, 3] |
| [1, 3, 5, 7]    | [0, 4] |

- 입출력 예 #1
  → [1, 2, 3, 4, 5]에는 짝수가 2, 4로 두 개, 홀수가 1, 3, 5로 세 개 있습니다.

- 입출력 예 #2
  → [1, 3, 5, 7]에는 짝수가 없고 홀수가 네 개 있습니다.

#### 📌 문제

```java
class Solution {
    public int[] solution(int[] num_list) {
        int[] answer = {};
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int[] solution(int[] num_list) {
        int[] answer = new int[2];

        for(int i = 0; i<num_list.length; i++){
            if(num_list[i] % 2 == 0){
                answer[0] += 1;
            }else{
                answer[1] += 1;
            }
        }
        return answer;
    }
}
```

for문으로 num_list의 length만큼 i를 증가시키면서 각 num_list의 0번째 인덱스부터 배열을 순회하여  
짝수일경우에는 answer[0]에 1을더해주고, 홀수일경우에는 answer[1]에 1을 더해주었다.

---

#### 💡 다른사람의 풀이

```java
class Solution {
    public int[] solution(int[] num_list) {
        int[] answer = new int[2];

        for(int i = 0; i < num_list.length; i++)
            answer[num_list[i] % 2]++;

        return answer;
    }
}
```

와 똑똑하당..!  
처음에 이해가 안가서 계속 보았다.  
어차피 answer는 2개짜리 배열이다.  
짝수일때는 0번째 배열에 1씩 더하고,  
홀수일때는 1번째 배열에 1씩 더한다

핸들링하는 값은 0과 1뿐이다..!  
answer에 num_list[0] % 2는 0이므로 answer[0]이고, 1++ 하였다  
answer에 num_list[1] % 2는 1이므로 answer[1]이고, 1++ 하였다  
answer에 num_list[2] % 2는 0이므로 answer[0]이고, 1++ 하였다  
....
이런식으로 0과 1의 배열의 값을 한개씩 증가시켰다
