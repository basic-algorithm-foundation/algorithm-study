# [주사위 게임3](https://school.programmers.co.kr/learn/courses/30/lessons/181916)
```java
import java.lang.Math;
import java.util.Map;
import java.util.HashMap;
import java.util.Set;

class Solution {
    public int solution(int a, int b, int c, int d) {

        // init
        Map<Integer, Integer> map = new HashMap<>();
        push(a, map);
        push(b, map);
        push(c, map);
        push(d, map);

        if (map.size() == 1) { // a, b, c, d 모두 같을 경우 1111 * p
            return 1111 * a;
        } else if (map.size() == 2) {
            if (map.containsValue(3)) { // a, b, c가 같고 d는 다른 수가 나오면 (10 * p + q)(10 * p + q)
                int p = 0;
                int q = 0;
                for (Integer key: map.keySet()) {
                    if (map.get(key) == 3) {
                        p = key;
                    }
                    if (map.get(key) == 1) {
                        q = key;
                    }
                }
                return ((10 * p) + q)*((10 * p) + q);
            } else { // a, b가 같고 c,d가 같을 경우
                int p = 0;
                int q = 0;
                int[] arr = map.keySet().stream().mapToInt(Integer::intValue).toArray();
                p = arr[0];
                q = arr[1];
                return (p + q) * Math.abs(p - q);
            }
        } else if (map.size() == 3) { // a, b == p, c == q, d== r 이면 q * r
            for(Integer key: Set.copyOf(map.keySet())) {
                if (map.get(key) == 2) {
                    map.remove(key);
                }
            }

            int[] arr = map.keySet().stream().mapToInt(Integer::intValue).toArray();
            int q = arr[0];
            int r = arr[1];
            return q * r;
        } else { // 모두 다르면 가장 작은 숫자
            return Math.min(Math.min(a, b), Math.min(c, d));
        }
    }

    public void push(int num, Map<Integer, Integer> map) {
        if (!map.containsKey(num)) {
            map.put(num, 1);
        } else {
            int v = map.get(num) + 1;
            map.put(num, v);
        }
    }
}
```

- 알게된 점
1. 컬렉션 프레임워크에 익숙해져야겠다. 
2. 리팩토링 가능한 부분을 찾아보자. 