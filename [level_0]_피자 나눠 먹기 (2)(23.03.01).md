# [Lv.0] 피자 나눠 먹기(2)(23.03.01)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120815

#### 📌 문제 설명

머쓱이네 피자가게는 피자를 여섯 조각으로 잘라 줍니다. 피자를 나눠먹을 사람의 수 `n`이 매개변수로 주어질 때, `n`명이 주문한 피자를 남기지 않고 모두 같은 수의 피자 조각을 먹어야 한다면 최소 몇 판을 시켜야 하는지를 return 하도록 solution 함수를 완성해보세요.

#### 📌 제한 조건

- 1 ≤ n ≤ 100

#### 📌 예시

| n   | result |
| --- | ------ |
| 6   | 1      |
| 10  | 5      |
| 4   | 2      |

- 입출력 예 #1
  → 6명이 모두 같은 양을 먹기 위해 한 판을 시켜야 피자가 6조각으로 모두 한 조각씩 먹을 수 있습니다.

- 입출력 예 #2
  → 10명이 모두 같은 양을 먹기 위해 최소 5판을 시켜야 피자가 30조각으로 모두 세 조각씩 먹을 수 있습니다.

- 입출력 예 #3
  → 4명이 모두 같은 양을 먹기 위해 최소 2판을 시키면 피자가 12조각으로 모두 세 조각씩 먹을 수 있습니다.

#### 📌 문제

```java
class Solution {
    public int solution(int n) {
        int answer = 0;
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
	public int solution(int n) {
		int answer = 1;

        while(answer * 6 % n != 0){
            answer++;
        }

		return answer;
	}
}
```

answer는 피자의 갯수고 n이 1일 경우에도 1이 반환되어야 하므로 answer = 0; 에서 answer = 1로 수정해주었다.
그리고 피자의 조각수(answer \* 6)이 n으로 나눴을때 나누어떨어지지 않을 경우에는 계속 피자의 갯수를 증가시켜주었다.
