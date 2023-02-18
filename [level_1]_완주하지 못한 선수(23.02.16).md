# [Lv.1] 완주하지 못한 선수(23.02.16)

#### 📌 URL : https://school.programmers.co.kr/learn/courses/30/lessons/42576

#### 📌 문제 설명

수많은 마라톤 선수들이 마라톤에 참여하였습니다. 단 한 명의 선수를 제외하고는 모든 선수가 마라톤을 완주하였습니다.  
마라톤에 참여한 선수들의 이름이 담긴 배열 participant와 완주한 선수들의 이름이 담긴 배열 completion이 주어질 때, 완주하지 못한 선수의 이름을 return 하도록 solution 함수를 작성해주세요.

#### 📌 제한 조건

- 마라톤 경기에 참여한 선수의 수는 1명 이상 100,000명 이하입니다.
- completion의 길이는 participant의 길이보다 1 작습니다.
- 참가자의 이름은 1개 이상 20개 이하의 알파벳 소문자로 이루어져 있습니다.
- 참가자 중에는 동명이인이 있을 수 있습니다.

#### 📌 예시

| participant                                       | completion                               | return   |
| ------------------------------------------------- | ---------------------------------------- | -------- |
| ["leo", "kiki", "eden"]                           | ["eden", "kiki"]                         | "leo"    |
| ["marina", "josipa", "nikola", "vinko", "filipa"] | ["josipa", "filipa", "marina", "nikola"] | "vinko"  |
| ["mislav", "stanko", "mislav", "ana"]             | ["stanko", "ana", "mislav"]              | "mislav" |

#### 📌 문제

```java
class Solution {
    public String solution(String[] participant, String[] completion) {
        String answer = "";
        return answer;
    }
}
```

---

#### ✏️ 풀이

```java
import java.util.Arrays;
class Solution {
    public String solution(String[] participant, String[] completion) {
        String answer = "";
        Arrays.sort(participant);
        Arrays.sort(completion);

        if(completion.length == 0){
            answer = participant[0];
        }
        for(int i = 0; i < completion.length; i++) {
            if(!(participant[i].equals(completion[i]))) {
                answer = participant[i];
                break;
            }
            if(i == completion.length-1){
                answer = participant[i+1];
            }
        }

        return answer;
    }
}
```

원래는 해시맵을 이용하라는 문제라고 한다.  
나는 아직 해시맵을 잘 모르기때문에 Arrays.sort를 사용하였다.  
두 배열을 오름차순으로 정렬한 뒤,  
for문으로 더 짧은 배열인 completion의 length만큼 participant를 돌리면서 각 i번째 인덱스만큼 비교하였다.  
만약 두개의 index의 요소가 일치하지 않을 경우에는 일치하지 않는 i번째 인덱스의 participant를 반환하도록 하였다.  
그리고 만약에 completion의 length 끝까지 일치하지 않는 요소를 찾지 못했다면, participant의 가장 마지막 사람이 완주하지 못한 사람이므로  
participant의 가장 마지막 index를 반환하도록 하고  
이부분은 놓친 부분인데 참가자가 1명이고, 완주자가 없는경우 completion의 배열이 없으므로 participant의 0번째 index를 반환하도록 처리하였다.

---

#### 💡 다른사람 풀이

```java
import java.util.Arrays;
class Solution {
    public String solution(String[] participant, String[] completion) {
        String answer = "";
        Arrays.sort(participant);
        Arrays.sort(completion);


        for(int i = 0; i < completion.length; i++) {
            if(!(participant[i].equals(completion[i]))) {
                return participant[i];
            }
        }
            return participant[participant.length-1];
    }
}
```

나와 함께 스터디 하시는 팀원분의 코드이다
참가자가 1명이고 완주자가 없는경우도 participant의 length-1번째 참가자를 반환하고,  
completion의 length만큼 for문을 반복하였는데 없는 경우네는 participant의 가장 마지막 사람, 즉 length-1번째의 사람을 반환하는 내용은 똑같으므로  
이 코드를 한번에 작성하신 내용이다 for안에서 if가 아니고, for문 바깥에서 작성하셔서 두가지 케이스를 모두 체크할수 있었다.

```java
//나중에 공부하기 위해 해시맵 코드도 추가
import java.util.HashMap;

class Solution {
    public String solution(String[] participant, String[] completion) {
        String answer = "";
        HashMap<String, Integer> hm = new HashMap<>();
        for (String player : participant) hm.put(player, hm.getOrDefault(player, 0) + 1);
        for (String player : completion) hm.put(player, hm.get(player) - 1);

        for (String key : hm.keySet()) {
            if (hm.get(key) != 0){
                answer = key;
            }
        }
        return answer;
    }
}
```
