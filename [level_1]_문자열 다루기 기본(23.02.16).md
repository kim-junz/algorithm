# [Lv.1] 문자열 다루기 기본(23.02.16)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/12918

#### 📌 문제 설명

문자열 s의 길이가 4 혹은 6이고, 숫자로만 구성돼있는지 확인해주는 함수, solution을 완성하세요. 예를 들어 s가 "a234"이면 False를 리턴하고 "1234"라면 True를 리턴하면 됩니다.

#### 📌 제한 조건

- `s`는 길이 1 이상, 길이 8 이하인 문자열입니다.
- `s`는 영문 알파벳 대소문자 또는 0부터 9까지 숫자로 이루어져 있습니다.

#### 📌 예시

| s      | return |
| ------ | ------ |
| "a234" | false  |
| "1234" | true   |

#### 📌 문제

```java
class Solution {
    public boolean solution(String s) {
        boolean answer = true;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public boolean solution(String s) {
        boolean answer = true;

            char[] ch = s.toCharArray();

            if(ch.length == 4 || ch.length == 6){
                for(char c : ch){
                    if(c > 65){
                    answer = false;
                    }
                }
            }else{
                answer = false;
            }
        return answer;
    }
}
```

문제가 헷갈렸는데 s의 길이가 4혹은 6이어야하고, 또 그중에서 숫자로만 구성되어있으면 true를 반환하고,  
문자열의 길이가 4 또는 6이 아닐경우, 4 또는 6이어도 숫자로만 되어있지 않은 경우에는 false를 반환 > 이었음

먼저 문자열의 길이가 4 또는 6이면, 문자인지 숫자인지 확인하는데,  
문자열을 char형 배열로 만들었고 알파벳은 65이상이므로, 65보다 클 경우에는 false를 반환하고 그렇지 않은경우는 그대로 answer의 true값을 반환,  
또 4또는 6이 아닐경우에는 무조건 false를 반환하도록 작성

코드를 어떻게 더 잘 하면 줄일수도있을것 같은데 ㅠㅠ
