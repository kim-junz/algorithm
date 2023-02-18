# [Lv.1] 핸드폰 번호 가리기(23.02.15)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/12948

#### 📌 문제 설명

정수를 담고 있는 배열 arr의 평균값을 return하는 함수, solution을 완성해보세요.  
프로그래머스 모바일은 개인정보 보호를 위해 고지서를 보낼 때 고객들의 전화번호의 일부를 가립니다.  
전화번호가 문자열 phone_number로 주어졌을 때, 전화번호의 뒷 4자리를 제외한 나머지 숫자를 전부 `*`으로 가린 문자열을 리턴하는 함수, solution을 완성해주세요.

#### 📌 제한 조건

- phone_number는 길이 4 이상, 20이하인 문자열입니다.

#### 📌 예시

| phone_number  | return           |
| ------------- | ---------------- |
| "01033334444" | "**\*\*\***4444" |
| "027778888"   | "**\***8888"     |

#### 📌 문제

```java
class Solution {
    public String solution(String phone_number) {
        String answer = "";
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public String solution(String phone_number) {
        String answer = "";

        String pre = "";
        String befo = "";

        pre = phone_number.substring(0, phone_number.length() -4);
        next = phone_number.substring(phone_number.length() -4, phone_number.length());

        answer = ("*").repeat(pre.length())+next;

        return answer;
    }
}

```

이전 문제에서 배운 substring과 repeat으로 0부터 문자열의 마지막에서 -4개를 뺀것까지 pre에 담고,  
문자열의 마지막에서 -4부터 마지막까지 뺀것은 next에 담아서 pre는 문자열의 갯수만큼 `*`를 반복하고 그 뒤에 next를붙임  
