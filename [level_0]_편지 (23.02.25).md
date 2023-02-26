# [Lv.0] 편지(23.02.25)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120898

#### 📌 문제 설명

머쓱이는 할머니께 생신 축하 편지를 쓰려고 합니다. 할머니가 보시기 편하도록 글자 한 자 한 자를 가로 2cm 크기로 적으려고 하며, 편지를 가로로만 적을 때, 축하 문구 `message`를 적기 위해 필요한 편지지의 최소 가로길이를 return 하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- 공백도 하나의 문자로 취급합니다.
- 1 ≤ message의 길이 ≤ 50
- 편지지의 여백은 생각하지 않습니다.
- `message`는 영문 알파벳 대소문자, ‘!’, ‘~’ 또는 공백으로만 이루어져 있습니다.

#### 📌 예시

| message           | result |
| ----------------- | ------ |
| "happy birthday!" | 30     |
| "I love you~"     | 22     |

- 입출력 예 #1
  → `message`의 글자 수가 15개로 최소 가로 30cm의 편지지가 필요합니다.

- 입출력 예 #2
  → `message`의 글자 수가 11개로 최소 가로 22cm의 편지지가 필요합니다.

#### 📌 문제

```java
class Solution {
    public int solution(String message) {
        int answer = 0;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int solution(String message) {
        int answer = 0;

        answer = message.length() * 2;
        return answer;
    }
}
```

편지지의 양 여백은 생각하지 않으니, 요소의 갯수에 2를 곱한 값을 반환해주면 되었다.
message는 String 타입이므로, length로 문자열의 갯수에 2를 곱하여 answer에 반환하였다.
