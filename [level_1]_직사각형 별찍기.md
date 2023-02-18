# [Lv.1] 직사각형 별찍기

### 📌 날짜 : 2023.02.15

### 📌 URL : https://programmers.co.kr/learn/courses/30/lessons/12969

### 📌 문제 설명

이 문제에는 표준 입력으로 두 개의 정수 n과 m이 주어집니다.별(\*) 문자를 이용해 가로의 길이가 n, 세로의 길이가 m인 직사각형 형태를 출력해보세요.

### 📌 제한 조건

n과 m은 각각 1000 이하인 자연수입니다.

### 📌 예시

- 입력 : 5, 3
- 출력 :

```
   *****
   *****
   *****
```

### 📌 문제

```java
import java.util.Scanner;

class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();

        System.out.println(a + b);
    }
}
```

---

### ✏️ 풀이

- ~~n과 m이랬는데 변수명은 a와 b네…~~
- ~~a+b는 왜써준거야…~~

```java
import java.util.Scanner;

class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();

        for(int i=0; i<b; i++){
            for(int j=0; j <a; j++){
                System.out.printf("*");
            }
            System.out.println();
        }

    }
}

```

나중에 받는 값 b가 열이 되니, 바깥 for문으로 돌려주고,  
먼저 받는 값 a가 행이 되니 안쪽 for문으로 반복하여 a만큼 \*이 찍히고  
안쪽 for를 빠져나오면 println으로 개행을 해주고,  
다시 i가 b만큼 되지 않았으면 해당 반복문을 반복하게 하여 직사각형 별을 찍어주었음

---

### 💡 다른사람의 풀이

```java
for (int i = 0; i < b; i++) {
      System.out.println("*".repeat(a));
}
```

행을 for문으로 찍어주고 열을 .repeat으로 반복해줌… 훨씬 간결하네
