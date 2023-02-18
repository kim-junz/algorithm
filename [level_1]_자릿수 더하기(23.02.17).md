# [Lv.1] 자릿수 더하기(23.02.17)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/12931

#### 📌 문제 설명

자연수 N이 주어지면, N의 각 자릿수의 합을 구해서 return 하는 solution 함수를 만들어 주세요.  
예를들어 N = 123이면 1 + 2 + 3 = 6을 return 하면 됩니다.

#### 📌 제한 조건

- N의 범위 : 100,000,000 이하의 자연수

#### 📌 예시

| N   | answer |
| --- | ------ |
| 123 | 6      |
| 987 | 24     |

#### 📌 문제

```java
import java.util.*;

public class Solution {
    public int solution(int n) {
        int answer = 0;

        // [실행] 버튼을 누르면 출력 값을 볼 수 있습니다.
        System.out.println("Hello Java");

        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
import java.util.*;

public class Solution {
    public int solution(int n) {
        int answer = 0;
        String str = Integer.toString(n);

        String ss = "";

        for(int i=0; i<str.length(); i++){
            ss = str.substring(i,i+1);
            answer += Integer.parseInt(ss);
        }

        return answer;
    }
}
```

먼저 int n을 `Integer.toString`으로 String으로 변환 후 , 해당 string을 for문으로 `substring`을 이용하여 String타입의 ss로 반환 후,  
ss를 `Integer.parseInt`로 다시 int로 변환하여 더해주었음  

