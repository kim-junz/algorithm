# [Lv.1] 가운데 글자 가져오기(23.02.15)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/12903

#### 📌 문제 설명

단어 s의 가운데 글자를 반환하는 함수, solution을 만들어 보세요. 단어의 길이가 짝수라면 가운데 두글자를 반환하면 됩니다.

#### 📌 제한 조건

s는 길이가 1 이상, 100이하인 스트링입니다.

#### 📌 예시

| s       | return |
| ------- | ------ |
| "abcde" | "c"    |
| "qwer"  | "we"   |

#### 📌 문제

```java
class Solution {
    public String solution(String s) {
        String answer = "";
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public String solution(String s) {
        String answer = "";

        if(s.length() % 2 ==0){
            answer = s.substring(s.length()/2-1, s.length()/2+1);
        }else{
            answer = s.substring(s.length()/2, s.length()/2+1);
        }
        return answer;
    }
}

```

substring() 메서드를 이용하여 원하는 시작지점, 원하는 끝지점을 지정하고 나머지 부분을 잘라내었음

짝수일경우 문자를 반으로 나눠서 그 앞 문자부터, 문자를 반으로 나눠서 그 뒤 문자까지 남기고 잘라내고  
홀수일경우 딱 반으로 안떨어지므로 2로 나눌경우 반으로 나눈것보다 1개 앞 문자를 시작지점으로 인지하므로-  
2로 나눠서 딱 가운데 문자부터 2+1번째 문자까지 하면 가운데문자만 남기고 잘라낼수 있게 됨.

나머지는 아래 예시 설명을 보면 좀 더 이해하기가 쉬울듯

---

#### ✅ substring() 문자 잘라내기 예시

- public String substring(int startIndex)\*\*
- public String substring(int startIndex, int endIndex)\*\*
