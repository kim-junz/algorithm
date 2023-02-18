# [Lv.1] 이상한 문자 만들기(23.02.17)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/12930

#### 📌 문제 설명

문자열 s는 한 개 이상의 단어로 구성되어 있습니다. 각 단어는 하나 이상의 공백문자로 구분되어 있습니다. 각 단어의 짝수번째 알파벳은 대문자로, 홀수번째 알파벳은 소문자로 바꾼 문자열을 리턴하는 함수, solution을 완성하세요.

#### 📌 제한 조건

- 문자열 전체의 짝/홀수 인덱스가 아니라, 단어(공백을 기준)별로 짝/홀수 인덱스를 판단해야합니다.
- 첫 번째 글자는 0번째 인덱스로 보아 짝수번째 알파벳으로 처리해야 합니다.

#### 📌 예시

| s                   | return              |
| ------------------- | ------------------- |
| "try hello world"   | "TrY HeLlO WoRlD"   |
| " try HELLO world " | " TrY HeLlO WoRlD " |

- 입출력 예시 설명
  → "try hello world"는 세 단어 "try", "hello", "world"로 구성되어 있습니다. 각 단어의 짝수번째 문자를 대문자로, 홀수번째 문자를 소문자로 바꾸면 "TrY", "HeLlO", "WoRlD"입니다. 따라서 "TrY HeLlO WoRlD" 를 리턴합니다.
  → 두번째 케이스는 내가 추가한 부분인데, 문자열이 모두 소문자가 아닐수도있고, 중간에 공백이 2개이상일수도 있다. 그리고 앞뒤로도 공백이 많을수도 있다. 이러한 부분을 모두 고려해서 코드를 작성해야한다.

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
        int idx = 0;

       char[] ch = s.toCharArray();

        for(int i=0; i<ch.length; i++){
            if(ch[i] == ' ') {
                answer += " ";
                idx = 0;
            }else{
                if (idx % 2 == 0) {
                    String k = String.valueOf(ch[i]);
                    k = k.toUpperCase();
                    answer += k;
                    idx++;
                } else {
                    String j = String.valueOf(ch[i]);
                    j = j.toLowerCase();
                    answer += j;
                    idx++;
                }
            }
        }

        return answer;
    }
}
```

이 문제는 내가 추가한 샘플 테스트케이스를 알기 전까지 맞게 처리하였는데 자꾸 오류가 나서 이유를 알수가 없었다.

- 모든 문자는 소문자로만 이루어져있지 않음
- 앞뒤로 공백이 있을 수 있으며, 공백을 제외하고 문자만으로 0번째부터 세어서 대소문자를 번갈아서 나타내주어야함
- 문자 중간에도 공백이 1개 이상 있을수도 있음

이 케이스들을 모두 고려해야했다.  
이부분은 1차적으로 기술매니저님께 조언을 구했는데,  
소문자 대문자를 일일이 판단하기가 복잡해지기때문에 `toUpperCase()` 또는 `toLowerCase()`처럼 모두 대문자로 바꾸거나, 모두 소문자로 바꿔서 시작해보라고 조언해주셨다. 각각의 메서드는 문자열을 Upper는 대문자로, Lower는 소문자로 모두 바꿔주는 메서드이다.

실제 배열이 갖고있는 인덱스값이 아닌 공백여부를 판단해서 문자일경우의 인덱스를 세어줘야해서 idx를 새로 선언해주었다.
그리고 배열이 공백이면 이 idx값을 초기화하였고,
짝수번째 알파벳일경우에는 대문자로, 홀수번째 알파벳일경우에는 소문자로만 출력되도록 메서드를 사용하였다.
처음에는 모두 대문자로 바꿔주고 시작해보았는데, 진행하다보니 굳이 미리 바꿔줄필요없고 0번부터 짝수번째에 있는 문자열을 모두 대문자로,  
1번부터 홀수번째에 있는 문자열은 모두 소문자로 바꿔주도록 하는것이 더 확실한것 같아 위와같이 코드를 변경하였다.

그리고 공백을 만나면 이 idx값은 다시 0부터 시작한다.
위와 같이 하였더니 성공..!

---

#### 💡 다른사람 풀이

문제가 특이했던만큼 신기한 코드들도 많이 나왔다.

```java
import java.util.Arrays;
class Solution {
  public String solution(String s) {

        String answer = "";
        int cnt = 0;
        String[] array = s.split("");

        for(String ss : array) {
            cnt = ss.contains(" ") ? 0 : cnt + 1;
            answer += cnt%2 == 0 ? ss.toLowerCase() : ss.toUpperCase();
        }
      return answer;
  }
}
```

split으로 ""를 하면 기준없이 모두 잘라낼수 있다는 사실을 알았다....
나머지는 바뀌기 전 코드인지 내용이 맞지않는것같다;

```java
class Solution {
    public String solution(String s) {
        String answer;
        answer = s.toUpperCase();
        char[] chars = answer.toCharArray();

        //앞문자가 대문자라면 소문자로 치환
        for (int i = 1; i < chars.length; i++) {
            if (62 <= chars[i - 1] && chars[i - 1] <= 90) {
                chars[i] = Character.toLowerCase(chars[i]);
            }
        }
        answer = String.valueOf(chars);
        return answer;
    }
}
```

이 코드는 앞문자가 대문자라면 소문자로 바꿔준다는 내용이 신기했다!
