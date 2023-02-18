# [Lv.1] 정수 내림차순으로 배치하기(23.02.17)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/12933

#### 📌 문제 설명

함수 solution은 정수 n을 매개변수로 입력받습니다. n의 각 자릿수를 큰것부터 작은 순으로 정렬한 새로운 정수를 리턴해주세요. 예를들어 n이 118372면 873211을 리턴하면 됩니다.

#### 📌 제한 조건

- n은 1이상 8000000000 이하인 자연수입니다.

#### 📌 예시

| n      | return |
| ------ | ------ |
| 118372 | 873211 |

#### 📌 문제

```java
class Solution {
    public long solution(long n) {
        long answer = 0;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
import java.util.Arrays;
import java.util.Collections;


class Solution {
    public long solution(long n) {
        String str = Long.toString(n);
        String[] s = new String[str.length()];
        long answer = 0;
        String res ="";

        for(int k= 0; k < str.length(); k++){
            s[k] = str.substring(k,k+1);
        }

        Arrays.sort(s, Collections.reverseOrder());

        for(String ss : s ){
            res += ss;
        }

        answer = Long.parseLong(res);
        return answer;
    }
}
```

앞서 다른 배열 문제들과 비슷하게 처리하였다. n을 Sting으로 변환 후, 배열로 바꿔 내림차순으로 정렬 후, String타입 res에 담았다.
해당 res를 answer에 숫자로 바꿔 저장하였다.

---

#### 💡 다른사람 풀이

```java
import java.util.*;

class Solution {
  public long solution(long n) {
        String[] list = String.valueOf(n).split("");
        Arrays.sort(list);

        StringBuilder sb = new StringBuilder();
        for (String aList : list) sb.append(aList);

        return Long.parseLong(sb.reverse().toString());
  }
}
```

문자열로 바꾸고 문자열 배열로 바꾸고 < 이부분을 한번에 처리하는 방법을 사용하셔서 가져와봤다.
String.valueOf()는 ()타입을 String타입으로 바꿔주는것이고, 또 이것을 바로 split("")를 통해 한글자씩 잘라서 String 배열에 넣어주었다.

그 아래부분은 왜 sort해주었는지 모르겠고;;(sort하란 말은 없었다..)
