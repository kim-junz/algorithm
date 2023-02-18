# [Lv.1] x만큼 간격이 있는 n개의 숫자(23.02.16)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/12954

#### 📌 문제 설명

함수 solution은 정수 x와 자연수 n을 입력 받아, x부터 시작해 x씩 증가하는 숫자를 n개 지니는 리스트를 리턴해야 합니다. 다음 제한 조건을 보고, 조건을 만족하는 함수, solution을 완성해주세요.

#### 📌 제한 조건

- x는 -10000000 이상, 10000000 이하인 정수입니다.
- n은 1000 이하인 자연수입니다.

#### 📌 예시

| x   | n   | answer       |
| --- | --- | ------------ |
| 2   | 5   | [2,4,6,8,10] |
| 4   | 4   | [4,8,12]     |
| -4  | 3   | [-4, -8]     |

#### 📌 문제

```java
class Solution {
    public long[] solution(int x, int n) {
        long[] answer = {};
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public long[] solution(int x, int n) {
        long num = x;
        long[] answer = new long[n];


        for(int i = 0; i < answer.length; i++){
            answer[i] = num;
            num += x;
        }

        return answer;
    }
}

```

X는 -10000000 이상, 10000000이하 정수 > long으로 선언해주고, for문으로 answer의 i번째 index에 num을 추가, 이후로 반복할때마다 num에 x를 계속 더해주었음
