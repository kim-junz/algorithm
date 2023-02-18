# [Lv.1] 문자열 내 p와 y의 개수(23.02.16)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/12916

#### 📌 문제 설명

대문자와 소문자가 섞여있는 문자열 s가 주어집니다. s에 'p'의 개수와 'y'의 개수를 비교해 같으면 True, 다르면 False를 return 하는 solution를 완성하세요. 'p', 'y' 모두 하나도 없는 경우는 항상 True를 리턴합니다. 단, 개수를 비교할 때 대문자와 소문자는 구별하지 않습니다.  
예를 들어 s가 "pPoooyY"면 true를 return하고 "Pyy"라면 false를 return합니다.

#### 📌 제한 조건

- 문자열 s의 길이 : 50 이하의 자연수
- 문자열 s는 알파벳으로만 이루어져 있습니다.

#### 📌 예시

| s         | answer |
| --------- | ------ |
| "pPoooyY" | true   |
| "Pyy"     | false  |

- 입출력 예 #1
  → 'p'의 개수 2개, 'y'의 개수 2개로 같으므로 true를 return 합니다.
- 입출력 예 #2
  → ‘p'의 개수 1개, 'y'의 개수 2개로 다르므로 false를 return 합니다.

#### 📌 문제

```java
class Solution {
    boolean solution(String s) {
        boolean answer = true;

        // [실행] 버튼을 누르면 출력 값을 볼 수 있습니다.
        System.out.println("Hello Java");

        return answer;
    }
}
//???
```

---

#### ✏️ 풀이

```java
class Solution {
    boolean solution(String s) {
        boolean answer = true;
        int p = 0;
        int y = 0;

        char[] ch = s.toCharArray();
        for(char c : ch){
            if(c == 'p' || c == 'P'){
                p++;
            }
            if(c=='y' || c=='Y'){
                y++;
            }
        }

        answer = y == p ? true : false;

        return answer;
    }
}
```

String을 배열로 만들기 위해 toCharArray를 이용하였다.  
char형 배열이 된 ch를 for문으로 반복하면서 p또는 P가 있을경우 P를 1 증가시켜주고,  
y또는 Y가 있을경우 y를 증가시켜, 둘의 수가 같을경우는 true를 아닐경우는 false를 반환하도록 삼항 연산자를 사용하였다.

---

#### 💡 다른사람의 풀이

```java
class Solution {
    boolean solution(String s) {
        s = s.toLowerCase();
        int count = 0;

        for (int i = 0; i < s.length(); i++) {

            if (s.charAt(i) == 'p')
                count++;
            else if (s.charAt(i) == 'y')
                count--;
        }

        if (count == 0)
            return true;
        else
            return false;
    }
}
```

애초에 모든 문자를 소문자 또는 대문자로 바꿔주고하면 소문자인지 대문자인지 구별안해도 되니 이부분은 나중에 활용해도 좋을것같다.

```java
class Solution {
    boolean solution(String s) {

        return s.replaceAll("[^yY]", "").length() - s.replaceAll("[^pP]", "").length() == 0 ? true : false;
    }
}
```

정규식을 이용한 풀이라고 하는데,
replaceAll()은 정규표현식을 사용하기가 가능하다고 한다. 정규표현식은 좀 더 공부를 해야할것같다.
