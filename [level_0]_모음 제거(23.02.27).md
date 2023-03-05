# [Lv.0] 모음 제거(23.02.27)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120849

#### 📌 문제 설명

영어에선 a, e, i, o, u 다섯 가지 알파벳을 모음으로 분류합니다. 문자열 `my_string`이 매개변수로 주어질 때 모음을 제거한 문자열을 return하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- `my_string`은 소문자와 공백으로 이루어져 있습니다.
- 1 ≤ `my_string`의 길이 ≤ 1,000

#### 📌 예시

| my_string          | result      |
| ------------------ | ----------- |
| "bus"              | "bs"        |
| "nice to meet you" | "nc t mt y" |

- 입출력 예 #1
  → "bus"에서 모음 u를 제거한 "bs"를 return합니다.

- 입출력 예 #2
  → "nice to meet you"에서 모음 i, o, e, u를 모두 제거한 "nc t mt y"를 return합니다.

#### 📌 문제

```java
class Solution {
    public String solution(String my_string) {
        String answer = "";
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public String solution(String my_string) {
        String answer = "";
        String res = "";
        char[] arr = my_string.toCharArray();

        char[] c = new char[]{'a', 'e', 'i', 'o', 'u'};
           for(int i=0; i<arr.length; i++){
               res = String.valueOf(arr[i]);
               for(int j=0; j<c.length; j++){
                    if(arr[i] == c[j]){
                        res ="";
                    }
                }
                    answer += res;
            }
        return answer;
    }
}
```

먼저 문자열을 char배열로 만들고, 같은 char형으로 모음 배열을 생성하였다  
그리고 for문을 통해 arr에 c배열과 일치하는 문자가 있을경우 빈값을 반환하여 더해주었다.

---

#### 💡 다른사람의 풀이

```java
class Solution {
    public String solution(String my_string) {
        String answer = "";
        answer = my_string.replaceAll("[aeiou]", "");
        // answer = my_string.replaceAll("[a,e,i,o,u]","");
        return answer;
    }
}
```

와 나는 for문으로 어렵게 해결했는데..! 메서드가 있었다
.replaceAll()

- String replaceAll(String regex, String replacement)
- replaceAll() 함수는 대상 문자열을 원하는 문자 값으로 변환하는 함수이다.
- 첫번째 매개변수는 변환하고자 하는 대상이 될 문자열
- 두번째 매개변수는 변환할 문자 값

이렇게 배열로도 가능한지는 처음알았네, 저렇게 대괄호로 묶어서 컴마도없이도 가능했다......
정말 신기한 코딩의세계
