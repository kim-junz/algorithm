# [Lv.0] 숫자 찾기(23.03.09)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120904

#### 📌 문제 설명

정수 `num`과 `k`가 매개변수로 주어질 때, `num`을 이루는 숫자 중에 `k`가 있으면 `num`의 그 숫자가 있는 자리 수를 return하고 없으면 -1을 return 하도록 solution 함수를 완성해보세요.

#### 📌 제한 조건

- 0 < `num` < 1,000,000
- 0 ≤ `k` < 10
- `num`에 `k`가 여러 개 있으면 가장 처음 나타나는 자리를 return 합니다.

#### 📌 예시

| num    | k   | result |
| ------ | --- | ------ |
| 29183  | 1   | 3      |
| 232443 | 4   | 4      |
| 123456 | 7   | -1     |

- 입출력 예 #1
  → 29183에서 1은 3번째에 있습니다.

- 입출력 예 #2
  → 232443에서 4는 4번째에 처음 등장합니다.

- 입출력 예 #3
  → 123456에 7은 없으므로 -1을 return 합니다.

#### 📌 문제

```java
class Solution {
    public int solution(int num, int k) {
        int answer = 0;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int solution(int num, int k) {
        int answer = -1;

        String str = num + "";

        for(int i = 0; i<str.length(); i++){
            String s = str.substring(i,i+1);
            int res = Integer.parseInt(s);
            if(res == k) {
                answer = i + 1;
                break;
            }
        }
        return answer;
    }
}
```

num을 String타입으로 바꿔준 다음 for문에서 substring으로 한개씩 떼어냈다.  
떼어낸 요소를 int형으로 바꾼다음, k와 비교했을때 일치하는게 있을경우 해당 i+1값을 반환하도록 하였다.  
answer를 -1로 초기화하여, 일치하는경우가 없을때는 -1을 반환하도록 하였음
