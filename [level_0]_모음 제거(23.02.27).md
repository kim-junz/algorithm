# [Lv.0] ๋ชจ์ ์ ๊ฑฐ(23.02.27)

#### ๐ URL : https://school.programmers.co.kr/learn/courses/30/lessons/120849

#### ๐ ๋ฌธ์  ์ค๋ช

์์ด์์  a, e, i, o, u ๋ค์ฏ ๊ฐ์ง ์ํ๋ฒณ์ ๋ชจ์์ผ๋ก ๋ถ๋ฅํฉ๋๋ค. ๋ฌธ์์ด `my_string`์ด ๋งค๊ฐ๋ณ์๋ก ์ฃผ์ด์ง ๋ ๋ชจ์์ ์ ๊ฑฐํ ๋ฌธ์์ด์ returnํ๋๋ก solution ํจ์๋ฅผ ์์ฑํด์ฃผ์ธ์.

#### ๐ ์ ํ ์กฐ๊ฑด

- `my_string`์ ์๋ฌธ์์ ๊ณต๋ฐฑ์ผ๋ก ์ด๋ฃจ์ด์ ธ ์์ต๋๋ค.
- 1 โค `my_string`์ ๊ธธ์ด โค 1,000

#### ๐ ์์

| my_string          | result      |
| ------------------ | ----------- |
| "bus"              | "bs"        |
| "nice to meet you" | "nc t mt y" |

- ์์ถ๋ ฅ ์ #1
  โ "bus"์์ ๋ชจ์ u๋ฅผ ์ ๊ฑฐํ "bs"๋ฅผ returnํฉ๋๋ค.

- ์์ถ๋ ฅ ์ #2
  โ "nice to meet you"์์ ๋ชจ์ i, o, e, u๋ฅผ ๋ชจ๋ ์ ๊ฑฐํ "nc t mt y"๋ฅผ returnํฉ๋๋ค.

#### ๐ ๋ฌธ์ 

```java
class Solution {
    public String solution(String my_string) {
        String answer = "";
        return answer;
    }
}
```

---

#### โ๏ธ ํ์ด

```java
class Solution {
    public String solution(String my_string) {
        String answer = "";
        String res = "";
        char[] arr = my_string.toCharArray();

        char[] c = new char[]{'a', 'e', 'i', 'o', 'u'};
           for(int i=0; i<arr.length; i++){
               res = String.valueOf(arr[i]);
               for(int j=0; j<c.length; j++){
                    if(arr[i] == c[j]){
                        res ="";
                    }
                }
                    answer += res;
            }
        return answer;
    }
}
```

๋จผ์  ๋ฌธ์์ด์ char๋ฐฐ์ด๋ก ๋ง๋ค๊ณ , ๊ฐ์ charํ์ผ๋ก ๋ชจ์ ๋ฐฐ์ด์ ์์ฑํ์๋ค  
๊ทธ๋ฆฌ๊ณ  for๋ฌธ์ ํตํด arr์ c๋ฐฐ์ด๊ณผ ์ผ์นํ๋ ๋ฌธ์๊ฐ ์์๊ฒฝ์ฐ ๋น๊ฐ์ ๋ฐํํ์ฌ ๋ํด์ฃผ์๋ค.

---

#### ๐ก ๋ค๋ฅธ์ฌ๋์ ํ์ด

```java
class Solution {
    public String solution(String my_string) {
        String answer = "";
        answer = my_string.replaceAll("[aeiou]", "");
        // answer = my_string.replaceAll("[a,e,i,o,u]","");
        return answer;
    }
}
```

์ ๋๋ for๋ฌธ์ผ๋ก ์ด๋ ต๊ฒ ํด๊ฒฐํ๋๋ฐ..! ๋ฉ์๋๊ฐ ์์๋ค
.replaceAll()

- String replaceAll(String regex, String replacement)
- replaceAll() ํจ์๋ ๋์ ๋ฌธ์์ด์ ์ํ๋ ๋ฌธ์ ๊ฐ์ผ๋ก ๋ณํํ๋ ํจ์์ด๋ค.
- ์ฒซ๋ฒ์งธ ๋งค๊ฐ๋ณ์๋ ๋ณํํ๊ณ ์ ํ๋ ๋์์ด ๋  ๋ฌธ์์ด
- ๋๋ฒ์งธ ๋งค๊ฐ๋ณ์๋ ๋ณํํ  ๋ฌธ์ ๊ฐ

์ด๋ ๊ฒ ๋ฐฐ์ด๋ก๋ ๊ฐ๋ฅํ์ง๋ ์ฒ์์์๋ค, ์ ๋ ๊ฒ ๋๊ดํธ๋ก ๋ฌถ์ด์ ์ปด๋ง๋์์ด๋ ๊ฐ๋ฅํ๋ค......
์ ๋ง ์ ๊ธฐํ ์ฝ๋ฉ์์ธ๊ณ
