# [Lv.0] 배열의 유사도(23.02.23)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120903

#### 📌 문제 설명

두 배열이 얼마나 유사한지 확인해보려고 합니다. 문자열 배열 `s1`과 `s2`가 주어질 때 같은 원소의 개수를 return하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- 1 ≤ s1, s2의 길이 ≤ 100
- 1 ≤ s1, s2의 원소의 길이 ≤ 10
- s1과 s2의 원소는 알파벳 소문자로만 이루어져 있습니다
- s1과 s2는 각각 중복된 원소를 갖지 않습니다.

#### 📌 예시

| numbers         | s2                          | result |
| --------------- | --------------------------- | ------ |
| ["a", "b", "c"] | ["com", "b", "d", "p", "c"] | 2      |
| ["n", "omg"]    | ["m", "dot"]                | 0      |

- 입출력 예 #1
  → "b"와 "c"가 같으므로 2를 return합니다.

- 입출력 예 #2
  → 같은 원소가 없으므로 0을 return합니다.

#### 📌 문제

```java
class Solution {
    public int solution(String[] s1, String[] s2) {
        int answer = 0;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int solution(String[] s1, String[] s2) {
        int answer = 0;

        for(int i =0; i<s1.length; i++){
            for(int j=0; j<s2.length; j++){
                answer += s1[i].equals(s2[j]) ? 1:0;
            }
        }

        return answer;
    }
}
```

s1의 배열의 요소와 s2의 배열요소 전부를 한개씩 비교해 본 후,  
같은것이 있을경우에는 answer에 1을 더해주고, 아닐경우에는 0을더해주어 같은 요소가 몇개가 있는지 반환하였다
