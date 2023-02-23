# [Lv.0] 문자열 뒤집기(23.02.21)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120822

#### 📌 문제 설명

문자열 `my_string`이 매개변수로 주어집니다. `my_string`을 거꾸로 뒤집은 문자열을 return하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- 1 ≤ my_string의 길이 ≤ 1,000

#### 📌 예시

| my_string | return  |
| --------- | ------- |
| "jaron"   | "noraj" |
| "bread"   | "daerb" |

- 입출력 예 #1
  → `my_string`이 "jaron"이므로 거꾸로 뒤집은 "noraj"를 return합니다.

- 입출력 예 #2
  → `my_string`이 "bread"이므로 거꾸로 뒤집은 "daerb"를 return합니다.

#### 📌 문제

```java
class Solution {
    public String solution(String my_string) {
        String answer = "";
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public String solution(String my_string) {
        String answer = "";

        String[] s = my_string.split("");

        for(int i = my_string.length()-1; i >= 0; i--){
            answer += s[i];
        }
        return answer;
    }
}
```

문자열 my_string을 split으로 잘라서 String 배열 s에 넣어준 후,  
for문으로 i를 my_string의 length로 초기화하고, 반복할때마다 i--를 해주었다.  
이렇게 할 경우 맨 마지막에 있는 배열부터 answer에 들어가게 되어 문자열을 뒤집을 수 있다.

---

#### 💡 다른사람의 풀이

```java
class Solution {
    public String solution(String my_string) {
        StringBuilder sb = new StringBuilder();
        sb.append(my_string);
        return sb.reverse().toString();
    }
}
```

StringBuilder를 사용할경우 .reverse로 쉽게 구현할 수 있다고 한다.  
아직 StringBuilder와 관련된 메서드들을 배우진 않았지만 참고하고자 추가하였다.
