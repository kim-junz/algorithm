# [Lv.0] 자릿수 더하기(23.02.25)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120906

#### 📌 문제 설명

정수 `n`이 매개변수로 주어질 때 `n`의 각 자리 숫자의 합을 return하도록 solution 함수를 완성해주세요

#### 📌 제한 조건

- 0 ≤ n ≤ 1,000,000

#### 📌 예시

| n      | result |
| ------ | ------ |
| 1234   | 10     |
| 930211 | 16     |

- 입출력 예 #1
  → 1 + 2 + 3 + 4 = 10을 return합니다.

- 입출력 예 #2
  → 9 + 3 + 0 + 2 + 1 + 1 = 16을 return합니다.

#### 📌 문제

```java
class Solution {
    public int solution(int n) {
        int answer = 0;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int solution(int n) {
        int answer = 0;
        String str = Integer.toString(n);

        for(int i =0; i<str.length(); i++){
            answer += Integer.parseInt(str.substring(i, i+1));
        }
        return answer;
    }
}
```

int인 n의 값을 String으로 바꾸어 str에 넣어주었다.  
그리고 for문을 통해 str을 substring으로 한글자씩 떼어, Integer.parseInt로 int로 변환하여 answer에 더해주어 값을 반환하였다
