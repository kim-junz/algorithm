# [Lv.0] 문자 반복 출력하기(23.02.22)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120889

#### 📌 문제 설명

문자열 `my_string`과 정수 n이 매개변수로 주어질 때, `my_string`에 들어있는 각 문자를 n만큼 반복한 문자열을 return 하도록 solution 함수를 완성해보세요.

#### 📌 제한 조건

- 2 ≤ my_string 길이 ≤ 5
- 2 ≤ n ≤ 10
- "my_string"은 영어 대소문자로 이루어져 있습니다.

#### 📌 예시

| my_string | n   | result            |
| --------- | --- | ----------------- |
| "hello"   | 3   | "hhheeellllllooo" |

- 입출력 예 #1
  → "hello"의 각 문자를 세 번씩 반복한 "hhheeellllllooo"를 return 합니다.

#### 📌 문제

```java
class Solution {
    public String solution(String my_string, int n) {
        String answer = "";
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public String solution(String my_string, int n) {
        String answer = "";

        for(int i =0; i<my_string.length(); i++){
            for(int j=0; j<n; j++ ){
                String str = my_string.substring(i, i+1);
                answer += str;
            }
        }

        return answer;
    }
}
```

my_string을 for문으로 substring으로 한글자씩 자르도록 하고,  
2중 for문으로 해당 문자열을 n번 반복하여 answer에 더해주었다
