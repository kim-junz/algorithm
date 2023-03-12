# [Lv.0] 문자열 정렬하기 (1)(23.03.02)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120850

#### 📌 문제 설명

문자열 `my_string`이 매개변수로 주어질 때, `my_string`안에 있는 숫자만 골라 오름차순 정렬한 리스트를 return 하도록 solution 함수를 작성해보세요.

#### 📌 제한 조건

- 1 ≤ `my_string`의 길이 ≤ 100
- `my_string`에는 숫자가 한 개 이상 포함되어 있습니다.
- `my_string`은 영어 소문자 또는 0부터 9까지의 숫자로 이루어져 있습니다.

#### 📌 예시

| my_string   | result          |
| ----------- | --------------- |
| "hi12392"   | [1, 2, 2, 3, 9] |
| "p2o4i8gj2" | [2, 2, 4, 8]    |
| "abcde0"    | [ 0 ]           |

- 입출력 예 #1
  → "hi12392"에 있는 숫자 1, 2, 3, 9, 2를 오름차순 정렬한 [1, 2, 2, 3, 9]를 return 합니다.

- 입출력 예 #2
  → "p2o4i8gj2"에 있는 숫자 2, 4, 8, 2를 오름차순 정렬한 [2, 2, 4, 8]을 return 합니다.

- 입출력 예 #3
  → "abcde0"에 있는 숫자 0을 오름차순 정렬한 [0]을 return 합니다.

#### 📌 문제

```java
class Solution {
    public int[] solution(String my_string) {
        int[] answer = {};
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
import java.util.ArrayList;
import java.util.Collections;

class Solution {
    public int[] solution(String my_string) {
       ArrayList<Integer> res = new ArrayList<>();
        char[] ch = my_string.toCharArray();

       for(int i=0; i < ch.length; i++){
           if(ch[i] < 58){
               String s = String.valueOf(ch[i]);
               int a = Integer.parseInt(s);
               res.add(a);
           }
       }

        Collections.sort(res);

        int[] answer = new int[res.size()];
        for(int i = 0; i < res.size(); i++) {
            answer[i] = res.get(i);
        }
        return answer;
    }
}
```

Inter타입의 ArrayList를 선언하고, my_string을 char배열로 변환하였다.  
for문을 통해 char배열의 i번째 인덱스가 58보다 작은경우(문자가 아닌경우)는 문자열 타입으로 바꿔주고,  
또 그 문자열 타입을 다시 int타입으로 바꿔 add하였다.

Collections는 List를 대상으로 하는 메서드들을 제공하는데, ArrayList인 res sort하였다.  
그리고 int타입의 배열 answer를 res.size와 같은 크기로 배열을 생성한 후,  
배열을 복사하였다. 증말 최대의 발악이었음 ㅠㅠ

---

#### 💡 다른사람의 풀이

```java
import java.util.*;

class Solution {
    public int[] solution(String my_string) {

        my_string = my_string.replaceAll("[a-z]","");

        int[] answer = new int[my_string.length()];

        for(int i =0; i<my_string.length(); i++){
            answer[i] = my_string.charAt(i) - '0';
        }

        Arrays.sort(answer);

        return answer;
    }
}

```

replaceAll은 파라미터 앞의 값을, 파라미터 뒤의 값으로 모두 변경해주는 메서드다.  
[a-z]는 정규식으로 소문자 a부터 z까지를 말한다. 문제의 조건에 문자는 소문자라고 하였으니, 소문자들을 모두 ""공백으로 바꿔주어 my_string에 저장한것이다.

그리고 배열 answer를 my_string의 length만큼 선언해주고,  
for문을 통해 answer의 i번째 인덱스에 charAt으로 my_string의 i번째 인덱스를 char형으로 바꾼다.  
바꾼 char형은 모두 숫자인 아스키코드값을 갖고있는데, '0'을 빼줄경우 정수 값만 남게된다.  
예를들면 '0'은 48이므로, 49인 '1'은 1의 값만 남게되고, 50인 '2'는 2의 값만 남게되는것이다.

그리고 answer sort후 반환...! 새로운 방법을 알게되었다.
