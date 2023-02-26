# [Lv.0] 배열 원소의 길이(23.02.20)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120854

#### 📌 문제 설명

문자열 배열 `strlist`가 매개변수로 주어집니다. `strlist` 각 원소의 길이를 담은 배열을 retrun하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- 1 ≤ `strlist` 원소의 길이 ≤ 100
- `strlist`는 알파벳 소문자, 대문자, 특수문자로 구성되어 있습니다.

#### 📌 예시

| strlist                        | result       |
| ------------------------------ | ------------ |
| ["We", "are", "the", "world!"] | [2, 3, 3, 6] |
| ["I", "Love", "Programmers."]  | [1, 4, 12]   |

- 입출력 예 #1
  → ["We", "are", "the", "world!"]의 각 원소의 길이인 [2, 3, 3, 6]을 return합니다.

- 입출력 예 #2
  → ["I", "Love", "Programmers."]의 각 원소의 길이인 [1, 4, 12]을 return합니다.

#### 📌 문제

```java
class Solution {
    public int[] solution(String[] strlist) {
        int[] answer = {};
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int[] solution(String[] strlist) {
        int[] answer = new int[strlist.length];

        for(int i=0; i < strlist.length; i++){
            answer[i] = strlist[i].length();
        }
        return answer;
    }
}
```

for문으로 0부터 시작하는 i값으로 배열을 돌리고  
answer[i]에 strlist배열의 i번째 요소의 length값을 넣어주었다.
