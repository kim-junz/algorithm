# [Lv.0] 직각 삼각형 출력하기(23.03.05)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120823

#### 📌 문제 설명

`*`의 높이와 너비를 1이라고 했을 때, `*`을 이용해 직각 이등변 삼각형을 그리려고합니다. 정수 `n` 이 주어지면 높이와 너비가 `n` 인 직각 이등변 삼각형을 출력하도록 코드를 작성해보세요.

#### 📌 제한 조건

- 1 ≤ `n`≤ 10

#### 📌 예시

- 입력 #1

```java
3
```

- 출력 #1

```java
*
**
***

```

- 입출력 예 #1
  → n이 3이므로 첫째 줄에 _ 1개, 둘째 줄에 _ 2개, 셋째 줄에 \* 3개를 출력합니다.

#### 📌 문제

```java
import java.util.Scanner;

public class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        System.out.println(n);
    }
}
```

---

#### ✏️ 풀이

```java
import java.util.Scanner;

public class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

         for(int i=0; i < n; i++){
            for(int j=0; j <= i; j++){
                System.out.printf("*");
            }
         System.out.println();
        }
    }
}
```

저 마지막에 System.out.println(n);이거 왜넣어준거야... 이거때문에 자꾸 잘못출력되서 내가 뭐 잘못했나 했잖아;;;
그냥 이중포문인데 사실 내가 이중포문에 약함 ㅠㅠ
i를 0부터 n까지 반복하고, j가 i보다 작거나 같을경우에는 *을 찍어주는것...
n의 값을 3으로 가정하였을때,
처음에는 0이고 j도 0이기 때문에 *를 1개 찍음 그다음에는 i보다 j가 크기 때문에 빠져나와서 줄바꿈
그리고 i가 1일때, 안쪽 포문으로 들어와서 j는 0이므로 i보다 작아서 별 1개, 그리고 j가 1일때 i와 같으므로 별 1개 총 2개를 찍음
그다음엔 j가 i보다 커졌으므로 빠져나와서 줄을 바꿔주고 i가 2가 되고, j는 다시 0부터 2까지.. 총 3개의 별을 찍음
그리고 빠져나와서 줄 바꿔주고, i는 3보다 작아야하므로 반복 끝..!

---

#### 💡 다른사람의 풀이

```java
public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        for(int i=1; i<=n; i++){
            System.out.println("*".repeat(i));
        }
    }
```

repeat으로 반복하는 방법이 있지 않을까했었는데 내 능력이 안되어서 ㅠㅠ...
i가 1일때 i만큼 \*를 반복하는건데,
n을 또 3으로 가정하였을때 i가 1일때 1개,
i가 2일때 2개 i가 3일때 3개 찍어주는것임....
나는 왜이렇게 별찍기에 약하지 아오 짜증나
