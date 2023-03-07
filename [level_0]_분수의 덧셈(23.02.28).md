# [Lv.0] 분수의 덧셈(23.02.28)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/120808

#### 📌 문제 설명

첫 번째 분수의 분자와 분모를 뜻하는 `numer1`, `denom1`, 두 번째 분수의 분자와 분모를 뜻하는 `numer2`, `denom2`가 매개변수로 주어집니다. 두 분수를 더한 값을 기약 분수로 나타냈을 때 분자와 분모를 순서대로 담은 배열을 return 하도록 solution 함수를 완성해보세요.

#### 📌 제한 조건

- 0 <`numer1`, `denom1`, `numer2`, `denom2` < 1,000

#### 📌 예시

| numer1 | denom1 | numer2 | denom2 | result  |
| ------ | ------ | ------ | ------ | ------- |
| 1      | 2      | 3      | 4      | [5, 4]  |
| 9      | 2      | 1      | 3      | [29, 6] |

- 입출력 예 #1
  → 1 / 2 + 3 / 4 = 5 / 4입니다. 따라서 [5, 4]를 return 합니다.

- 입출력 예 #2
  → 9 / 2 + 1 / 3 = 29 / 6입니다. 따라서 [29, 6]을 return 합니다.

#### 📌 문제

```java
class Solution {
    public int[] solution(int numer1, int denom1, int numer2, int denom2) {
        int[] answer = {};
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public int[] solution(int numer1, int denom1, int numer2, int denom2) {
        int[] answer = new int[2];

        answer[0] = (numer1*denom2)+(denom1*numer2);
        answer[1] = denom1*denom2;

        int min = Math.min(answer[0], answer[1]);
        int max = Math.max(answer[0], answer[1]);

        while(min != 0){
            int r = max % min;
            max = min;
            min = r;
        }
        answer[0] /= max;
        answer[1] /= max;

        return answer;
    }
}
```

유클리드호제법을 사용하였다. 진짜 생전 듣도보도 못한 알고리즘인데.......  
진짜 도저히 답이 안나와서 최대공약수를 구하는 메서드가 있나 검색해보았는데 그런건 없고 유클리드호제법으로 구해야한다고 하였다.  
유클리드 호제법이란 아래와 같다....

`유클리드호제법`  
비교대상의 두 개의 자연수 a와 b에서(단 a>b) a를 b로 나눈 나머지를 r이라고 했을때 GCD(a, b) = GCD(b, r)과 같고 "r이 0이면 그때 b가 최대공약수이다."라는 원리를 활용한 알고리즘입니다.  
예) GCD(24,16) -> GCD(16,8) -> GCD(8,0) : 최대공약수 = 8

일단 두 분모와 분자를 더하는 방법에 대해서는 굳이 설명하지 않겠다(이건알겠지)  
일단 분모와 분자중에서 어떤 수가 더 크고 작은지 모르기때문에 두 수 중에서 큰 수를 max에 작은수를 min에 넣고,  
유클리드 호제법에 따라서 int r은 max를 min으로 나눈 나머지를 넣고, max에는 min값을, min에는 r을 대입하였다  
그리고 이는 while문을 통해 min이 0이될때까지 반복하였다.

왜 그런지 증명에 관한 부분은 나무위키를 보았는데 사실 무슨소리인지 하나도 모르겠다 ㅠㅠ
공식만 외워야지....

---

#### 💡 다른사람의 풀이

```java
class Solution {
    public int[] solution(int denum1, int num1, int denum2, int num2) {
        int[] answer = new int[2];

        answer[0]=denum1*num2+denum2*num1;
        answer[1]=num1*num2;

        for(int i=answer[1]; i >= 1; i--){
            if(answer[0]%i==0 && answer[1]%i==0){
                answer[0] /= i;
                answer[1] /= i;
            }
        }

        return answer;
    }
}
```

풀이를 보니 유클리드호제법을 사용하지 않고도 해결하신분이 계셨다.  
분모를 기준으로 분모가 0이될때까지 i를 --하면서 반복하였다  
만약 분자와 분모를 둘다 나눴을때 나머지가 0이 되는 i값이 있다면 각 분모, 분자를 나눠주기를 반복하여 더이상 나눠질 수 없을정도로 약분한 후 반환하였다  
수학만 알고있다면 유클리드호제법을 사용하지 않고도 구현할수 있었겠지만.....
나는 너무 담을쌓았나 ㅠㅠ
