# [Lv.1] 짝수와 홀수(23.02.15)

#### 📌 URL : https://programmers.co.kr/learn/courses/30/lessons/12937

#### 📌 문제 설명

정수 num이 짝수일 경우 "Even"을 반환하고 홀수인 경우 "Odd"를 반환하는 함수, solution을 완성해주세요.

#### 📌 제한 조건

- num은 int 범위의 정수입니다.
- 0은 짝수입니다.

#### 📌 예시

| num | return |
| --- | ------ |
| 3   | "Odd"  |
| 4   | "Even" |

#### 📌 문제

```java
class Solution {
    public String solution(int num) {
        String answer = "";
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public String solution(int num) {
        String answer = "";

        if(num % 2 == 0){
            answer = "Even";
        }else{
            answer = "Odd";
        }

        return answer;
    }
}

```

num을 2로 나눴을때 나머지가 0일경우에는 Even을 반환하고,  
그렇지 않은경우는 Odd를 반환하도록 함
