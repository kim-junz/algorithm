# [Lv.0] 배열 회전시키기(23.03.07)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120844

#### 📌 문제 설명

정수가 담긴 배열 `numbers`와 문자열 `direction`가 매개변수로 주어집니다. 배열 `numbers`의 원소를 `direction`방향으로 한 칸씩 회전시킨 배열을 return하도록 solution 함수를 완성해주세요.

#### 📌 제한 조건

- 3 ≤ `numbers`의 길이 ≤ 20
- `direction`은 "left" 와 "right" 둘 중 하나입니다.

#### 📌 예시

| numbers                   | direction | result                    |
| ------------------------- | --------- | ------------------------- |
| [1, 2, 3]                 | "right"   | [3, 1, 2]                 |
| [4, 455, 6, 4, -1, 45, 6] | "left"    | [455, 6, 4, -1, 45, 6, 4] |

- 입출력 예 #1
  → numbers 가 [1, 2, 3]이고 direction이 "right" 이므로 오른쪽으로 한 칸씩 회전시킨 [3, 1, 2]를 return합니다.

- 입출력 예 #2
  → numbers 가 [4, 455, 6, 4, -1, 45, 6]이고 direction이 "left" 이므로 왼쪽으로 한 칸씩 회전시킨 [455, 6, 4, -1, 45, 6, 4]를 return합니다.

#### 📌 문제

```java
class Solution {
    public int[] solution(int[] numbers, String direction) {
        int[] answer = {};
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int[] solution(int[] numbers, String direction) {
        int[] answer = new int[numbers.length];
        
          for(int i =0; i< numbers.length-1; i++){
            if(direction.equals("left")){
                answer[i] = numbers[i+1];
                answer[answer.length-1] = numbers[0];
            }else{
                answer[0] = numbers[numbers.length-1];
                answer[i+1] = numbers[i];
            }
        }
        return answer;
    }
}
```
완전 지저분하게 풀은것같은데, 이 외에 다른 방법이 있는지는 모르겠다 ㅠㅠ    
다른사람의 풀이를 봐도 ArrayList 사용한것 외에는... 딱히 엄청난 코드도없었고,   
ArrayList는 나도 사용하고싶은데 이상하게 내가 사용하면 오류남;;;    

먼저, for문을 numbers의 length-1만큼 반복해주었다    
answer도 numbers와 같은 length이겠지만, 복사할 배열은 left일 경우 마지막, right일경우 맨 처음 인덱스 값은 직접넣어줄것이기 때문에...   

left일경우에는    
answer의 0번째 인덱스부터 numbers의 1번째 인덱스부터 복사해서 넣고,   
answer의 가장 마지막 인덱스에는 numbers의 0번째 인덱스 값을 넣었다   

right일 경우에는    
answer의 0번째 인덱스에 numbers의 마지막 인덱스 값을 넣었고,   
answer의 i+1번째 인덱스, 즉 1번째 인덱스부터 numbser의 0번째 인덱스의 값을 차례대로 복사하였다   

