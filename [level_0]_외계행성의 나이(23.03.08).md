# [Lv.0] 외계행성의 나이(23.03.08)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120834

#### 📌 문제 설명

우주여행을 하던 머쓱이는 엔진 고장으로 PROGRAMMERS-962 행성에 불시착하게 됐습니다. 입국심사에서 나이를 말해야 하는데, PROGRAMMERS-962 행성에서는 나이를 알파벳으로 말하고 있습니다. a는 0, b는 1, c는 2, ..., j는 9입니다. 예를 들어 23살은 cd, 51살은 fb로 표현합니다. 나이 `age`가 매개변수로 주어질 때 PROGRAMMER-962식 나이를 return하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- `age`는 자연수입니다.
- `age` ≤ 1,000
- PROGRAMMERS-962 행성은 알파벳 소문자만 사용합니다.

#### 📌 예시

| age | result |
| --- | ------ |
| 23  | "cd"   |
| 51  | "fb"   |
| 100 | "baa"  |

- 입출력 예 #1
  → age가 23이므로 "cd"를 return합니다.

- 입출력 예 #2
  → age가 51이므로 "fb"를 return합니다.

- 입출력 예 #3
  → age가 100이므로 "baa"를 return합니다.

#### 📌 문제

```java
class Solution {
    public String solution(int age) {
        String answer = "";
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public String solution(int age) {
        String answer = "";

        String str = age+"";
        char[] ch = str.toCharArray();

        for(char c : ch){
            answer += String.valueOf((char)(c + '1'));
        }

        return answer;
    }
}
```

먼저 int타입인 age를 String으로 바꾸기 위해 String str에 age와 +""를 더하여 String타입으로 만든 다음 저장해주었다.  
그리고 str을 char 배열로 바꿔준다음에, 각 요소에 '1'을 더하고(49) 그 char를 String으로 바꿔 answer로 반환하였다
