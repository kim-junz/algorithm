# [Lv.1] 수박수박수박수박수박수?(23.02.16)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/12922

#### 📌 문제 설명

길이가 n이고, "수박수박수박수...."와 같은 패턴을 유지하는 문자열을 리턴하는 함수, solution을 완성하세요. 예를들어 n이 4이면 "수박수박"을 리턴하고 3이라면 "수박수"를 리턴하면 됩니다.

#### 📌 제한 조건

- n은 길이 10,000이하인 자연수입니다.

#### 📌 예시

| n   | return     |
| --- | ---------- |
| 3   | "수박수"   |
| 4   | "수박수박" |

#### 📌 문제

```java
class Solution {
    public String solution(int n) {
        String answer = "";
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public String solution(int n) {
        String answer = "";
        String[] s = {"수","박"};

        for(int i=0; i < n; i++){
            if(i % 2 == 0){
                answer += s[0];
            }else{
                answer += s[1];
            }
        }
        return answer;
    }
}
```

String 배열에 "수"와 "박"을 넣고,  
for문으로 n번까지 i를 증가시키는데, 여기서 i가 0부터 시작하였으니, 0을 2로 나눈 값이 0으로 짝수번째가 "수"가 되고 홀수번째가"박"이 되어  
answer에 문자열을 붙여주었다.
