# [Lv.1] 서울에서 김서방 찾기(23.02.16)

#### 📌 URL : https://programmers.co.kr/learn/courses/30/lessons/12919

#### 📌 문제 설명

String형 배열 seoul의 element중 "Kim"의 위치 x를 찾아, "김서방은 x에 있다"는 String을 반환하는 함수, solution을 완성하세요. seoul에 "Kim"은 오직 한 번만 나타나며 잘못된 값이 입력되는 경우는 없습니다.

#### 📌 제한 조건

- seoul은 길이 1 이상, 1000 이하인 배열입니다.
- seoul의 원소는 길이 1 이상, 20 이하인 문자열입니다.
- "Kim"은 반드시 seoul 안에 포함되어 있습니다.

#### 📌 예시

| seoul           | return              |
| --------------- | ------------------- |
| ["Jane", "Kim"] | "김서방은 1에 있다" |

- 입출력 예 #1
  → 이용금액이 3인 놀이기구를 4번 타고 싶은 고객이 현재 가진 금액이 20이라면, 총 필요한 놀이기구의 이용 금액은 30(= 3+6+9+12) 이 되어 10만큼 부족하므로 10을 return 합니다.

#### 📌 문제

```java
class Solution {
    public String solution(String[] seoul) {
        String answer = "";
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
class Solution {
    public String solution(String[] seoul) {
        String answer = "";

            for(int i =0; i < seoul.length; i++){
            boolean b = seoul[i].equals("Kim") ? true : false;

            if(b == true){
                answer = "김서방은 "+i+"에 있다";
            }
        }
        return answer;
    }
}
```

for문으로 seoul을 돌려서 seoul의[i]번째에 있는 값이 "Kim"과 일치하면 true를 일치하지 않으면 false를 반환하는 b를 선언하였고,  
b가 true일 경우 i값을 가져왔다.
