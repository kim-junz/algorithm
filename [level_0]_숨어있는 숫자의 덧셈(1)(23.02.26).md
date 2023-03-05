# [Lv.0] 숨어있는 숫자의 덧셈 (1)(23.02.26)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120851

#### 📌 문제 설명

문자열 `my_string`이 매개변수로 주어집니다. `my_string`안의 모든 자연수들의 합을 return하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- 1 ≤ `my_string`의 길이 ≤ 1,000
- `my_string`은 소문자, 대문자 그리고 한자리 자연수로만 구성되어있습니다.
- 연속된 숫자도 각각 한 자리 숫자로 취급합니다.

#### 📌 예시

| my_string       | result |
| --------------- | ------ |
| "aAb1B2cC34oOp" | 10     |
| "1a2b3c4d123"   | 16     |

- 입출력 예 #1
  → "aAb1B2cC34oOp"안의 한자리 자연수는 1, 2, 3, 4 입니다. 따라서 1 + 2 + 3 + 4 = 10 을 return합니다.

- 입출력 예 #2
  → "1a2b3c4d123Z"안의 한자리 자연수는 1, 2, 3, 4, 1, 2, 3 입니다. 따라서 1 + 2 + 3 + 4 + 1 + 2 + 3 = 16 을 return합니다.

#### 📌 문제

```java
class Solution {
    public int solution(String my_string) {
        int answer = 0;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int solution(String my_string) {
        int answer = 0;

       char[] ch = my_string.toCharArray();

       for(char c : ch){
           if(c < 65) {
               String s = String.valueOf(c);
               answer += Integer.parseInt(s);
           }

       }
        return answer;
    }
}
```

toCharArray로 바꿔서 아스키코드를 이용하여 문자를 걸러낸 후 바로 answer에 넣고싶었는데 방법을 잘 몰랐다.  
위에처럼 진행해도 좋지만 변수를 하나 덜 선언하기 위해  
아래 코드처럼 바로 char를 Integer.partInt()로 '만들어서' 해도 좋은방법인것 같다

```java
class Solution {
    public int solution(String my_string) {
        int answer = 0;

       char[] ch = my_string.toCharArray();

       for(char c : ch){
           if(c < 65) {
               answer += Integer.parseInt(""+c);
           }
       }
        return answer;
    }
}
```

pareInt할때 String만 가능하니까 앞에 ""를 붙여 스트링처럼 만들어주었다.
