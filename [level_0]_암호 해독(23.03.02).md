# [Lv.0] 암호 해독(23.03.02)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120892

#### 📌 문제 설명

군 전략가 머쓱이는 전쟁 중 적군이 다음과 같은 암호 체계를 사용한다는 것을 알아냈습니다.

암호화된 문자열 `cipher`를 주고받습니다.  
그 문자열에서 `code`의 배수 번째 글자만 진짜 암호입니다.   
문자열 `cipher`와 정수 `code`가 매개변수로 주어질 때 해독된 암호 문자열을 return하도록 solution 함수를 완성해주세요.  

#### 📌 제한 조건

- 1 ≤ `cipher`의 길이 ≤ 1,000
- 1 ≤ `code` ≤ `cipher`의 길이
- `cipher`는 소문자와 공백으로만 구성되어 있습니다.
- 공백도 하나의 문자로 취급합니다.

#### 📌 예시

| cipher                     | code | result     |
| -------------------------- | ---- | ---------- |
| "dfjardstddetckdaccccdegk" | 4    | "attack"   |
| "pfqallllabwaoclk"         | 2    | "fallback" |

- 입출력 예 #1
  → "dfjardstddetckdaccccdegk" 의 4번째, 8번째, 12번째, 16번째, 20번째, 24번째 글자를 합친 "attack"을 return합니다.

- 입출력 예 #2
  → "pfqallllabwaoclk" 의 2번째, 4번째, 6번째, 8번째, 10번째, 12번째, 14번째, 16번째 글자를 합친 "fallback"을 return합니다.

#### 📌 문제

```java
class Solution {
    public String solution(String cipher, int code) {
        String answer = "";
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public String solution(String cipher, int code) {
        String answer = "";
        String[] str = cipher.split("");

        for(int i =1; i <= str.length; i++){
          answer += i % code == 0 ? str[i-1] : "";
        }

        return answer;
    }
}
```

먼저 cipher를 split으로 나누어 배열로 바꾼다음에 for문을 통해 암호를 추출하고자 하였다.  
int는 1부터 시작하고, i를 code로 나눴을때 나머지가 0일때만 str의 i-1번째값의 인덱스를 반환하고, 아닐때는 ""(빈칸)을 반환하도록 하였다.  

---

#### 💡 다른사람의 풀이

```java
class Solution {
    public String solution(String cipher, int code) {
        String answer = "";

        for (int i = code; i <= cipher.length(); i = i + code) {
            answer += cipher.substring(i - 1, i);
        }

        return answer;
    }
}
```

애초에 i를 code로 하고, i가 chpher의 length보다 작거나 같을경우 반복하면서, i에다가 i+code를 한다... 즉 code에 code를 더하는거니까 계속 2배, 3배가 되어가는거겠지  
그리고 answer에는 substring을 이용하여 cipher의 i-1번째부터 i번째까지 자른 문자열을 반환하는법....  
아이 내가 한거보다 더 짧고 좋아보이잖아...  
