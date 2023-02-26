# [Lv.0] 특정 문자 제거하기(23.02.20)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120831

#### 📌 문제 설명

문자열 `my_string`과 문자 `letter`이 매개변수로 주어집니다. `my_strin`g에서 `letter`를 제거한 문자열을 return하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- 1 ≤ `my_string`의 길이 ≤ 100
- `letter`은 길이가 1인 영문자입니다.
- `my_string`과 `letter`은 알파벳 대소문자로 이루어져 있습니다.
- 대문자와 소문자를 구분합니다.

#### 📌 예시

| my_string | letter | result  |
| --------- | ------ | ------- |
| "abcdef"  | "f"    | "abcde" |
| "BCBdbe"  | "B"    | "Cdbe"  |

- 입출력 예 #1
  → "abcdef" 에서 "f"를 제거한 "abcde"를 return합니다.

- 입출력 예 #2
  → "BCBdbe" 에서 "B"를 모두 제거한 "Cdbe"를 return합니다.

#### 📌 문제

```java
class Solution {
    public String solution(String my_string, String letter) {
        String answer = "";
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public String solution(String my_string, String letter) {
        String answer = "";

            for(int i =0; i < my_string.length(); i++) {
                String str = my_string.substring(i, i + 1);
                if (str.equals(letter) == true) {
                    continue;
                }
                answer += str;
            }
        return answer;
    }
}
```

substring으로 my_string을 한글자씩 떼서 비교하여 letter와 같을경우에는 continue하고 나머지는 더하여 answer에 반환하였다.

---

#### 💡 다른사람의 풀이

```java
class Solution {
    public String solution(String my_string, String letter) {
        return my_string.replace(letter, "");
    }
}
```

처음보는 메서드가 있어서 가져왔다.

- replace : 자신이 바꾸고싶은 문자로 문자열을 치환시켜줌  
  즉 replace는 문자열에서 원하는 문자를 바꾸고싶은 문자로 바꿔준다고 한다.  
  위 코드를 해석해보면 my_string에 있는 letter라는 문자를 ""(빈칸)으로 바꿔주었다는 내용이다!  
  너무 간단하고 신기하다
