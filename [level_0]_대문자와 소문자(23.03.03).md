# [Lv.0] 대문자와 소문자(23.03.02)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120893

#### 📌 문제 설명

문자열 `my_string`이 매개변수로 주어질 때, 대문자는 소문자로 소문자는 대문자로 변환한 문자열을 return하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- 1 ≤ `my_string`의 길이 ≤ 1,000
- `my_string`은 영어 대문자와 소문자로만 구성되어 있습니다.

#### 📌 예시

| my_string    | result     |
| ------------ | ---------- |
| "cccCCC"     | "CCCccc"   |
| "abCdEfghIJ" | "ABcDeFGHij" |

- 입출력 예 #1
  → 소문자는 대문자로 대문자는 소문자로 바꾼 "CCCccc"를 return합니다.

- 입출력 예 #2
  → 소문자는 대문자로 대문자는 소문자로 바꾼 "ABcDeFGHij"를 return합니다.

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
        char[] ch = my_string.toCharArray();

       for(int i=0; i < ch.length; i++){
           char a = ch[i] < 97 ? Character.toLowerCase(ch[i]) : Character.toUpperCase(ch[i]);
           answer += String.valueOf(a);
       }
        
        return answer;
    }
}
```

my_string을 toCharArray를 통해 char형 배열로 변환한다음 for문으로 배열을 하나씩 확인하며,    
만약 배열이 97보다 작을경우 (대문자일경우) toLowerCase를 적용하고, 아닌경우는 toUpperCase를 적용하도록 삼항연산자로 구현하였다.   
