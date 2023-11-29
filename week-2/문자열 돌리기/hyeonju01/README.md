# [문자열 돌리기](https://school.programmers.co.kr/learn/courses/30/lessons/181945)
```java
import java.util.Scanner;

public class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String a = sc.next();
        for(int i = 0; i < a.length(); i++) {
            System.out.println(a.charAt(i));
        }
    }
}
```
- 알게 된 점
1. String.length()와 array.length의 차이를 알아두자.
2. charAt()을 사용하는 연습을 해야겠다.