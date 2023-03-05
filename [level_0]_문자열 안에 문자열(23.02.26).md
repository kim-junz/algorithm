# [Lv.0] 문자열안에 문자열(23.02.26)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120908

#### 📌 문제 설명

문자열 `str1`, `str2`가 매개변수로 주어집니다. `str1` 안에 `str2`가 있다면 1을 없다면 2를 return하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- 1 ≤ `str1`의 길이 ≤ 100
- 1 ≤ `str2`의 길이 ≤ 100
- 문자열은 알파벳 대문자, 소문자, 숫자로 구성되어 있습니다.

#### 📌 예시

| str1                     | str2   | result |
| ------------------------ | ------ | ------ |
| "ab6CDE443fgh22iJKlmn1o" | "6CD"  | 10     |
| "ppprrrogrammers"        | "pppp" | 16     |
| "AbcAbcA"                | "AAA"  | 2      |

- 입출력 예 #1
  → "ab6CDE443fgh22iJKlmn1o" str1에 str2가 존재하므로 1을 return합니다.

- 입출력 예 #2
  → "ppprrrogrammers" str1에 str2가 없으므로 2를 return합니다.return합니다.

  - 입출력 예 #3
    → "AbcAbcA" str1에 str2가 없으므로 2를 return합니다.

#### 📌 문제

```java
class Solution {
    public int solution(String str1, String str2) {
        int answer = 0;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int solution(String str1, String str2) {
        int answer = 0;
        answer = str1.contains(str2) ? 1 : 2;
        return answer;
    }
}
```

아무리 for와 if를 써도 아래와 같을 경우 해결이 힘들었다 ㅠㅠ str2의 2번째글자까지는 일치하는데, 그 이후 한번 더 체크하려고하면 이미 str1의 문자열은 끝났기때문에 이런부분 포함해서 자꾸 예외, 예외, 예외를 만들어줘야했는데

```java
String str1 = "AbcAbcAA";
String str2 = "AAA";
```

문자열 안에 문자열을 포함하는지 확인하는 메서드가 있었다...-.-;  
.contains라는 메서드인데, 사용방법은 위에 풀이 코드를 보면 될것 같다.  
확인하고자 하는 문자열을 포함하고있을경우 true, 없을경우 false를 반환한다  
진짜 한번 메서드들 정리해야하는데..!
