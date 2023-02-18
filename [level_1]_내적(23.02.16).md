# [Lv.1] 내적(23.02.16)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/70128

#### 📌 문제 설명

길이가 같은 두 1차원 정수 배열 a, b가 매개변수로 주어집니다. a와 b의 [내적](https://en.wikipedia.org/wiki/Dot_product)을 return 하도록 solution 함수를 완성해주세요.
이때, a와 b의 내적은 `a[0]*b[0] + a[1]*b[1] + ... + a[n-1]*b[n-1]` 입니다. (n은 a, b의 길이)

#### 📌 제한 조건

- a, b의 길이는 1 이상 1,000 이하입니다.
- a, b의 모든 수는 -1,000 이상 1,000 이하입니다.

#### 📌 예시

| a         | b           | result |
| --------- | ----------- | ------ |
| [1,2,3,4] | [-3,-1,0,2] | 3      |
| [-1,0,1]  | [1,0,-1]    | -2     |

- 입출력 예 #1
  → a와 b의 내적은 1*(-3) + 2*(-1) + 3*0 + 4*2 = 3 입니다.
- 입출력 예 #2
  → a와 b의 내적은 (-1)*1 + 0*0 + 1*(-1) = -2 입니다.


#### 📌 문제

```java
class Solution {
    public int solution(int[] a, int[] b) {
        int answer = 1234567890;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int solution(int[] a, int[] b) {
        int answer = 0;
        
        for(int i=0; i<a.length; i++){
          answer += a[i]*b[i];   
        }
        
        return answer;
    }
}
```
 a배열과 b배열의 길이가 같고 각 i번째 index를 곱해서 answer에 더해주었다