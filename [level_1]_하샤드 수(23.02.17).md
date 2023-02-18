# [Lv.1] 하샤드 수(23.02.17)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/12947

#### 📌 문제 설명

양의 정수 x가 하샤드 수이려면 x의 자릿수의 합으로 x가 나누어져야 합니다. 예를 들어 18의 자릿수 합은 1+8=9이고, 18은 9로 나누어 떨어지므로 18은 하샤드 수입니다. 자연수 x를 입력받아 x가 하샤드 수인지 아닌지 검사하는 함수, solution을 완성해주세요.

#### 📌 제한 조건

- x는 1 이상, 10000 이하인 정수입니다.

#### 📌 예시

| arr | return |
| --- | ------ |
| 10  | true   |
| 12  | true   |
| 11  | false  |
| 13  | false  |

- 입출력 설명 #1  
   → 10의 모든 자릿수의 합은 1입니다. 10은 1로 나누어 떨어지므로 10은 하샤드 수입니다.
- 입출력 설명 #2  
   → 12의 모든 자릿수의 합은 3입니다. 12는 3으로 나누어 떨어지므로 12는 하샤드 수입니다.
- 입출력 설명 #1  
   → 11의 모든 자릿수의 합은 2입니다. 11은 2로 나누어 떨어지지 않으므로 11는 하샤드 수가 아닙니다.
- 입출력 설명 #2  
   → 13의 모든 자릿수의 합은 4입니다. 13은 4로 나누어 떨어지지 않으므로 13은 하샤드 수가 아닙니다.

#### 📌 문제

```java
class Solution {
    public boolean solution(int x) {
        boolean answer = true;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public boolean solution(int x) {
        boolean answer = true;
        int res = 0;

        String str = Integer.toString(x);

        for(int i =0; i < str.length(); i++){
            res += Integer.parseInt(str.substring(i, i+1));

        }
        answer = x % res == 0 ? true : false;
        return answer;
    }
}
```

먼저 int를 String으로 바꿔준 후, 해당 String을 substring으로 for문으로 잘라주어 다시 int타입으로 res에 더해주었다.
이 더해준 res로 x를 나눠 0이 되면 true, 0이 되지 않으면 false를 반환하도록 하였다.
