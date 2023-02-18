# [Lv.1] 행렬의 덧셈(23.02.15)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/12950

#### 📌 문제 설명

행렬의 덧셈은 행과 열의 크기가 같은 두 행렬의 같은 행, 같은 열의 값을 서로 더한 결과가 됩니다. 2개의 행렬 arr1과 arr2를 입력받아, 행렬 덧셈의 결과를 반환하는 함수, solution을 완성해주세요.

#### 📌 제한 조건

- 행렬 arr1, arr2의 행과 열의 길이는 500을 넘지 않습니다.

#### 📌 예시

| arr1          | arr2          | return        |
| ------------- | ------------- | ------------- |
| [[1,2],[2,3]] | [[3,4],[5,6]] | [[4,6],[7,9]] |
| [[1],[2]]     | [[3],[4]]     | [[4],[6]      |

#### 📌 문제

```java
class Solution {
    public int[][] solution(int[][] arr1, int[][] arr2) {
        int[][] answer = {};
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int[][] solution(int[][] arr1, int[][] arr2) {
        
        int[][] answer = new int[arr1.length][arr1[0].length];

        for(int i = 0; i < arr1.length; i++){
            for(int j = 0; j < arr1[i].length; j++){
                answer[i][j]=arr1[i][j]+arr2[i][j];
            }
        }
        return answer;
    }
}

```

2차배열이었음. for문을 이용하여 2차배열의 값을 가져와서 서로 더해주고 넣어주기만 하면됨  
answer를 처음에 초기화를 안해서 헤매었는데 배열은 초기화를 잘 해줘야함ㅠㅠ  
이부분의 개념은 이후 다시 잡고 풀었음  

- - -

#### 💡 다른사람의 풀이

a와 b를 따로 더해주지 않더라도, 바로 a에 b를 더한것을 return하는 풀이도 있었음.
