# [Lv.0] 세균 증식(23.03.04)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120910

#### 📌 문제 설명

어떤 세균은 1시간에 두배만큼 증식한다고 합니다. 처음 세균의 마리수 `n`과 경과한 시간 `t`가 매개변수로 주어질 때 `t`시간 후 세균의 수를 return하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- 1 ≤ `n`≤ 10
- 1 ≤ `t` ≤ 15

#### 📌 예시

| n   | t   | result  |
| --- | --- | ------- |
| 2   | 10  | 2048    |
| 7   | 15  | 229,376 |

- 입출력 예 #1
  → 처음엔 2마리, 1시간 후엔 4마리, 2시간 후엔 8마리, ..., 10시간 후엔 2048마리가 됩니다. 따라서 2048을 return합니다.

- 입출력 예 #2
  → 처음엔 7마리, 1시간 후엔 14마리, 2시간 후엔 28마리, ..., 15시간 후엔 229376마리가 됩니다. 따라서 229,376을 return합니다.

#### 📌 문제

```java
class Solution {
    public int solution(int n, int t) {
        int answer = 0;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int solution(int n, int t) {
        int answer = n;
       for(int i = 1; i <= t; i++){
           answer = answer * 2;
           System.out.println(answer);
       }
        return answer;
    }
}
```

알고리즘 안풀었다고 확실히 머리 굳어가는 기분이 든다 ㅠㅠ  
처음부터 n마리가 있었기 때문에 answer에 n을 대입해준다.  
그리고 for문을 통해 t와 작거나 같으면 반복을 시켜주고, 결국 t만큼 반복을 시켜준다는 뜻임..  
int i는 이미 n마리를 담고있는 상황이 0이기 때문에 1부터 시작을 해주고, answer를 *2를 해준 후, 그 값을 answer에 담고,  
그 다은 answer를 또 *2를 해주고 담고 하는 방법으로 t만큼 반복한 값을 리턴하였다.
