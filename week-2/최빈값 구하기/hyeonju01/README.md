# [최빈값 구하기](https://school.programmers.co.kr/learn/courses/30/lessons/120812)
```java
import java.util.*;

class Solution {
    public int solution(int[] array) {
        int mod = 0; // key
        int secondMod = -1; // key
        int maxModValue = -1; // value

        Map<Integer, Integer> modeMap = new HashMap<>();

        // {1: 1, 2:1, 3:3, 4:1}
        for(int num: array) {
            if (!modeMap.containsKey(num)) {
                modeMap.put(num, 1);
            } else {
                int v = modeMap.get(num);
                modeMap.put(num, v + 1);
            }
        }

        for (Integer key: modeMap.keySet()) {
            if (modeMap.get(key) > maxModValue) {
                maxModValue = modeMap.get(key);
                mod = key;

            } else if (modeMap.get(key) == maxModValue) {
                secondMod = key;
            }
        }

        if (modeMap.get(mod) == modeMap.get(secondMod)) {
            return -1;
        }

        return mod;

    }
}
```

- 알게된 점
풀었던 문제인데도 헤맸다.. 최빈값과 최빈값의 Key를 잘 구별하고, Map을 잘 사용할 줄 알아야 풀리는 문제였다.