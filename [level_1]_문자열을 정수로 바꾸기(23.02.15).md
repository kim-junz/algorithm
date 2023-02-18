# [Lv.1] 문자열을 정수로 바꾸기(23.02.15)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/12925

#### 📌 문제 설명

문자열 s를 숫자로 변환한 결과를 반환하는 함수, solution을 완성하세요.

#### 📌 제한 조건

- s의 길이는 1 이상 5이하입니다.
- s의 맨앞에는 부호(+, -)가 올 수 있습니다.
- s는 부호와 숫자로만 이루어져있습니다.
- s는 "0"으로 시작하지 않습니다.

#### 📌 예시

- 입출력 예:  
   예를들어 str이 "1234"이면 1234를 반환하고, "-1234"이면 -1234를 반환하면 됩니다.  
   str은 부호(+,-)와 숫자로만 구성되어 있고, 잘못된 값이 입력되는 경우는 없습니다.

#### 📌 문제

```java
class Solution {
    public int solution(String s) {
        int answer = 0;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int solution(String s) {
        int answer = 0;

        answer = Integer.parseInt(s);

        return answer;
    }
}

```

문자열을 integer로 바꿔주는 Integer.parseInt()를 이용했음  
본래는 int로 변환이 가능하지 않은 값이 들어올경우를 try/catch해줘야 하는데  
문제에서는 잘못된 값이 입력되는 경우는 없다고 하니 따로 예외처리를 해주지는 않았다
