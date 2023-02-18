# [Lv.1] 자연수 뒤집어 배열로 만들기(23.02.17)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/12932

#### 📌 문제 설명

자연수 n을 뒤집어 각 자리 숫자를 원소로 가지는 배열 형태로 리턴해주세요. 예를들어 n이 12345이면 [5,4,3,2,1]을 리턴합니다.

#### 📌 제한 조건

- n은 10,000,000,000이하인 자연수입니다.

#### 📌 예시

| N     | return      |
| ----- | ----------- |
| 12345 | [5,4,3,2,1] |

#### 📌 문제

```java
class Solution {
    public int[] solution(long n) {
        int[] answer = {};
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int[] solution(long n) {
        String str = Long.toString(n);

        int[] answer = new int[str.length()];
        String[] s = new String[str.length()];

        int num = str.length()-1;

        for(int k= 0; k < str.length(); k++){
            s[k] = str.substring(k,k+1);
        }

        for(int i = num, j = 0; i >= 0; i--,j++){
            answer[j] = Integer.parseInt(s[i]);
        }

        return answer;
    }
}
```

내 평범한 풀이..ㅠㅠ  
long으로 선언된 n을 String으로 바꿔서 String을 substring으로 잘라서 String배열에 넣고, 이 String 배열은 마지막 인덱스부터 복사해서 answer에 integer로 변환하여 넣었다.  

---

#### 💡 다른사람 풀이

int를 String으로 String을 String배열로, String 배열을 다시 int배열로 바꾸는게 너무 비효율적이어서 혹시 다른방법으로 어떻게 풀으셨나 팀원들께 조언을 구했는데,  
팀원분께서 문자열을 숫자로 바꾸거나 할때 toCharArray를 써서 char형으로 바꾸면 아스키코드를 이용하여 -n을 해주면 문자가 숫자로 바뀌니까 그런 방법을 나중에 적절한 문제가 나오면 써봐도 좋을것같다 해주셨다.  

```java
import java.util.stream.IntStream;

class Solution {
    public int[] solution(long n) {
        return new StringBuilder().append(n).reverse().chars().map(Character::getNumericValue).toArray();
    }
}
```

import된것 보면 stream을 쓴것 같다.  
stream을 쓰면 코드는 간결하지만 효율성은 떨어진다는것 같은데 아직 배우지 않아서 잘 모르겠다.  

그래도 코드가 간결해서 가져와봤다.  

```java
class Solution {
  public int[] solution(long n) {
      String s = String.valueOf(n);
      StringBuilder sb = new StringBuilder(s);
      sb = sb.reverse();
      String[] ss = sb.toString().split("");

      int[] answer = new int[ss.length];
      for (int i=0; i<ss.length; i++) {
          answer[i] = Integer.parseInt(ss[i]);
      }
      return answer;
  }
}
```

reverse() 메서드가 신기했다. 해당 메서드는 StringBuilder, StringBuffer 클래스에서 제공하는 메서드라고 한다.  
문자열을 뒤집을 수 있는 메서드라고한다.  
