# [배열 만들기 4](https://school.programmers.co.kr/learn/courses/30/lessons/181918)
```java
import java.util.*;

class Solution {
    public int[] solution(int l, int r) {
        List<Integer> list = new ArrayList<>();
        
        // 0, 5로만 이루어진 모든 정수 찾기..
        for (int i = l; i < r+1; i++) {
            int curNum = i;
            boolean containsZeroOrFive = false;
            while (curNum > 0) {
                int digit = curNum % 10;
                if (digit == 0 || digit == 5) {
                    containsZeroOrFive = true;
                } else {
                    containsZeroOrFive = false;
                    break;
                }
                curNum /= 10;
            }
            if (containsZeroOrFive) {
                list.add(i);
            }
        }
        if (list.isEmpty()) {
            list.add(-1);
            return list.stream().mapToInt(Integer::intValue).toArray();
        }
        
        return list.stream().mapToInt(Integer::intValue).toArray();
    }
}
```

- 알게된 점
1. 처음 접근할 때 숫자를 문자열로 바꾼 후 5를 포함하거나 0을 포함하는 경우로 찾았더니 525, 515.. 등의 의도하지 않은 값들이 걸러지지 않아 틀렸다.
2. 문자열로 바꿀 경우, 5나 0을 포함하는 정규표현식을 만들어서 regex 를 사용해야 하는데 익숙하지 않고 손에 익지 않을 것 같아서 풀이 및 gpt의 도움을 받았다.
3. 자릿수 하나하나 모두 비교해주는 charAt()으로 접근할 수 있다. 자릿수를 나누어 digit값이 0이거나 5일 때 boolean을 true로 두고, 수를 10으로 나누며 줄여가다가 어느 순간 한번이라도 0,5외 값이 나올 경우 boolean을 false로 바꾸고 boolean이 true일 때에만 list에 넣어주었더니 풀렸다.
