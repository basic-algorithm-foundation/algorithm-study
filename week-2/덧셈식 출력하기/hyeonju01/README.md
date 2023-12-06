# [덧셈식 출력하기](https://school.programmers.co.kr/learn/courses/30/lessons/181947)
```java
import java.io.*;
import java.util.*;

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

        StringTokenizer st = new StringTokenizer(br.readLine());

        int a = Integer.parseInt(st.nextToken());
        int b = Integer.parseInt(st.nextToken());
        int answer = a + b;
        System.out.println(a +" + " + b + " = "+ answer);
    }
}
```

- 알게된 점
풀었던 문제라서 Scanner 대신 BufferedReader를 사용하는 것으로 리팩토링하였다. 
라이브러리 Import, 예외 처리, 출력값 처리 등에 주의해야겠다. 
Scanner랑 BufferedReader의 성능 비교도 해보자!