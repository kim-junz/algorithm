# [Lv.0] 인덱스 바꾸기(23.03.06)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120895

#### 📌 문제 설명

문자열 `my_string`과 정수 `num1`, `num2`가 매개변수로 주어질 때, `my_string`에서 인덱스 `num1`과 인덱스 `num2`에 해당하는 문자를 바꾼 문자열을 return 하도록 solution 함수를 완성해보세요.

#### 📌 제한 조건

- 1 < `my_string`의 길이 < 100
- 0 ≤ `num1`, `num2` < `my_string`의 길이
- `my_string`은 소문자로 이루어져 있습니다.
- `num1` ≠ `num2`

#### 📌 예시

| my_string    | num1 | num2 | result       |
| ------------ | ---- | ---- | ------------ |
| "hello"      | 1    | 2    | "hlelo"      |
| "I love you" | 3    | 6    | "I l veoyou" |

- 입출력 예 #1
  → "hello"의 1번째 인덱스인 "e"와 2번째 인덱스인 "l"을 바꾸면 "hlelo"입니다.

- 입출력 예 #2
  → "I love you"의 3번째 인덱스 "o"와 " "(공백)을 바꾸면 "I l veoyou"입니다.

#### 📌 문제

```java
class Solution {
    public String solution(String my_string, int num1, int num2) {
        String answer = "";
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public String solution(String my_string, int num1, int num2) {
        String answer = "";

        String[] str = my_string.split("");

        String res = str[num1];
        str[num1] = str[num2];
        str[num2] = res;

        for(String s : str){
            answer += s;
        }

        return answer;
    }
}
```

my_string을 배열로 바꿔준다음, 각 인덱스의 위치에 바꿀 요소를 넣어주고 for문으로 다시 String으로 합쳐주었다.
