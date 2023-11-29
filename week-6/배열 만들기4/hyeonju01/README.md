# [배열 만들기 4](https://school.programmers.co.kr/learn/courses/30/lessons/181918)
```java
import java.util.List;
import java.util.ArrayList;

class Solution {
    public int[] solution(int[] arr) {
        List<Integer> stk = new ArrayList<>();
        
        int idx = 0;
        int stkSize;
        
        while(idx < arr.length) {
            stkSize = stk.size();
            if (stk.isEmpty()) {
                stk.add(arr[idx]);
                idx++;
            } else if (!stk.isEmpty() &&
                     stk.get(stkSize - 1) < arr[idx]) {
                stk.add(arr[idx]);
                idx ++;
            } else if(!stk.isEmpty() &&
                     stk.get(stkSize - 1) >= arr[idx]) {
                stk.remove(stkSize - 1);
            }
        }
        return stk.stream().mapToInt(Integer::intValue).toArray();
    }
}
```

- 알게된 점
1. idx를 다루는 변수의 경우, 초깃값에서 -1을 할 경우 인덱스 예외가 발생할 수 있으니, size를 구해 놓고 사용될 때 -1을 해야 한다.

1. 처음 접근할 때 숫자를 문자열로 바꾼 후 5를 포함하거나 0을 포함하는 경우로 찾았더니 525, 515.. 등의 의도하지 않은 값들이 걸러지지 않아 틀렸다.
2. 문자열로 바꿀 경우, 5나 0을 포함하는 정규표현식을 만들어서 regex 를 사용해야 하는데 익숙하지 않고 손에 익지 않을 것 같아서 풀이 및 gpt의 도움을 받았다.
3. 자릿수 하나하나 모두 비교해주는 charAt()으로 접근할 수 있다. 자릿수를 나누어 digit값이 0이거나 5일 때 boolean을 true로 두고, 수를 10으로 나누며 줄여가다가 어느 순간 한번이라도 0,5외 값이 나올 경우 boolean을 false로 바꾸고 boolean이 true일 때에만 list에 넣어주었더니 풀렸다.
