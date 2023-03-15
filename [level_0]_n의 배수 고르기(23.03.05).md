# [Lv.0] n의 배수 고르기(23.03.05)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120905

#### 📌 문제 설명

정수 `n`과 정수 배열 `numlist`가 매개변수로 주어질 때, `numlist`에서 `n`의 배수가 아닌 수들을 제거한 배열을 return하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- 1 ≤ `n` ≤ 10,000
- 1 ≤ `numlist`의 크기 ≤ 100
- 1 ≤ `numlist`의 원소 ≤ 100,000

#### 📌 예시

| n   | numlist                        | result             |
| --- | ------------------------------ | ------------------ |
| 3   | [4, 5, 6, 7, 8, 9, 10, 11, 12] | [6, 9, 12]         |
| 5   | [1, 9, 3, 10, 13, 5]           | [10, 5]            |
| 12  | [2, 100, 120, 600, 12, 12]     | [120, 600, 12, 12] |

- 입출력 예 #1
  → numlist에서 3의 배수만을 남긴 [6, 9, 12]를 return합니다.

- 입출력 예 #2
  → numlist에서 5의 배수만을 남긴 [10, 5]를 return합니다.

- 입출력 예 #3
  → numlist에서 12의 배수만을 남긴 [120, 600, 12, 12]를 return합니다.

#### 📌 문제

```java
class Solution {
    public int[] solution(int n, int[] numlist) {
        int[] answer = {};
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int[] solution(int n, int[] numlist) {
        int count = 0;
        int j=0;
        int[] answer = {};

        for(int i =0; i<numlist.length; i++){
           if(numlist[i] % n == 0){
               count++;
           }
        }

        answer = new int[count];
        for(int i =0; i<numlist.length; i++){
            if(numlist[i] % n == 0){
                answer[j] = numlist[i];
                j++;
            }
        }
        return answer;
    }
}
```

ArrayList가 안먹어서 다시 작성한 코드.........  
numlist에서 n의 배수의 갯수를 세어 count에 저장하고,  
count의 수만큼 answer배열을 생성한다  
그리고 다시 for문을 통해 answer배열에 if문으로 n의 배수만 걸러서 저장한다

---

#### 💡 다른사람의 풀이

```java
        ArrayList<Integer> answer = new ArrayList<>();

        for(int a : numlist){
            if(a % n ==0) {
                answer.add(a);
            }
        }
```

다른사람 아니고 내 풀이 ㅠㅠㅠ 예전에도 ArrayList로 풀었었는데, 프로그래머스에서는 자꾸 오류가 나서 적용을 못해봤는데 이번에도 그러네....
