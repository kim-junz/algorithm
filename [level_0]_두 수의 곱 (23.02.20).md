# [Lv.0] ๋ ์์ ๊ณฑ(23.02.20)

#### ๐ URL : https://school.programmers.co.kr/learn/courses/30/lessons/120804

#### ๐ ๋ฌธ์  ์ค๋ช

์ ์ `num1`, `num2`๊ฐ ๋งค๊ฐ๋ณ์ ์ฃผ์ด์ง๋๋ค. `num1`๊ณผ `num2`๋ฅผ ๊ณฑํ ๊ฐ์ return ํ๋๋ก solution ํจ์๋ฅผ ์์ฑํด์ฃผ์ธ์.

#### ๐ ์ ํ ์กฐ๊ฑด

- 0 < num1 โค 100
- 0 < num2 โค 100

#### ๐ ์์

| num1 | num2 | result |
| ---- | ---- | ------ |
| 3    | 4    | 12     |
| 27   | 19   | 513    |

- ์์ถ๋ ฅ ์ #1
  โ `num1`์ด 3, `num2`๊ฐ 4์ด๋ฏ๋ก 3 \* 4 = 12๋ฅผ returnํฉ๋๋ค.

- ์์ถ๋ ฅ ์ #2
  โ `num1`์ด 27, `num2`๊ฐ 19์ด๋ฏ๋ก 27 \* 19 = 513์ returnํฉ๋๋ค.

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

        answer = num1 * num2;
        return answer;
    }
}
```

num1์ num2๋ก ๊ณฑํ ๊ฒฐ๊ณผ๋ฅผ answer์ ๋ฐํ
