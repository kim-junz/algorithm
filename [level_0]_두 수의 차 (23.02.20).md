# [Lv.0] ๋ ์์ ์ฐจ(23.02.20)

#### ๐ URL : https://school.programmers.co.kr/learn/courses/30/lessons/120803

#### ๐ ๋ฌธ์  ์ค๋ช

์ ์ `num1`, `num2`๊ฐ ๋งค๊ฐ๋ณ์ ์ฃผ์ด์ง๋๋ค. `num1`๊ณผ `num2`๋ฅผ ๋บ ๊ฐ์ returnํ๋๋ก soltuion ํจ์๋ฅผ ์์ฑํด์ฃผ์ธ์.

#### ๐ ์ ํ ์กฐ๊ฑด

- -50000 < num1 โค 50000
- -50000 < num2 โค 50000

#### ๐ ์์

| num1 | num2 | result |
| ---- | ---- | ------ |
| 2    | 3    | -1     |
| 100  | 2    | 98     |

- ์์ถ๋ ฅ ์ #1
  โ `num1`์ด 2, `num2`๊ฐ 4์ด๋ฏ๋ก 2 - 3 = -1์ returnํฉ๋๋ค.

- ์์ถ๋ ฅ ์ #2
  โ `num1`์ด 100, `num2`๊ฐ 2์ด๋ฏ๋ก 100 - 2 = 98์ returnํฉ๋๋ค.

#### ๐ ๋ฌธ์ 

```java
class Solution {
    public int solution(int num1, int num2) {
        int answer = 0;
        return answer;
    }
}
```

---

#### โ๏ธ ํ์ด

```java
class Solution {
    public int solution(int num1, int num2) {
        int answer = 0;

        answer = num1 - num2;
        return answer;
    }
}
```

num1์์ num2๋ฅผ ๋บ ๊ฒฐ๊ณผ๋ฅผ answer์ ๋ฐํ
