# [Lv.0] 가위 바위 보(23.03.02)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120839

#### 📌 문제 설명

가위는 2 바위는 0 보는 5로 표현합니다. 가위 바위 보를 내는 순서대로 나타낸 문자열 `rsp`가 매개변수로 주어질 때, rsp에 저장된 가위 바위 보를 모두 이기는 경우를 순서대로 나타낸 문자열을 return하도록 solution 함수를 완성해보세요.   

#### 📌 제한 조건

- 0 < `rsp`의 길이 ≤ 100
- `rsp`와 길이가 같은 문자열을 return 합니다.
- `rsp`는 숫자 0, 2, 5로 이루어져 있습니다.

#### 📌 예시

| rsp   | result |
| ----- | ------ |
| "2"   | "0"    |
| "205" | "052"  |

- 입출력 예 #1
  → "2"는 가위이므로 바위를 나타내는 "0"을 return 합니다.

- 입출력 예 #2
  → "205"는 순서대로 가위, 바위, 보이고 이를 모두 이기려면 바위, 보, 가위를 순서대로 내야하므로 “052”를 return합니다.

#### 📌 문제

```java
class Solution {
    public String solution(String rsp) {
        String answer = "";
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public String solution(String rsp) {
        String answer = "";
        
        for(int i=0; i<rsp.length(); i++){
            String s = rsp.substring(i, i+1);
            answer += s.equals("2") ? "0" : s.equals("0") ? "5" : "2";
        }
        
        return answer;
    }
}
```

처음에는 for문 안에 switch문으로 하였는데, 좀 코드 줄 수를 줄이고 효율적으로 짤 수 있을것 같았다.   
그래서 생각하다가 저번에 여러개의 조건을 이어붙인 삼항연산자가 생각나서 적용해보았다.   
substring으로 자른 문자가 "2"와 같을 경우는 "0", 아닐경우에는 s가 "0"과 같을경우라면 "5" 그 나머지 경우는 "2"를 answer에 더하여 문자열을 반환하도록 하였다.   
