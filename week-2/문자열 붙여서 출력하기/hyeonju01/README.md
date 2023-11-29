# [문자열 붙여서 출력하기](https://school.programmers.co.kr/learn/courses/30/lessons/181946)
- 예전 풀이
```java
import java.util.Scanner;

public class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String a = sc.next();
        String b = sc.next();
    }
}
```

- 이번 풀이
```java
import java.util.Scanner;
import java.io.*;

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String a = br.readLine();
        a = a.replace(" ", "");
        System.out.println(a);
    }
}
```

- 알게 된 점
문자열 메서드는 바로 호출 가능하다.