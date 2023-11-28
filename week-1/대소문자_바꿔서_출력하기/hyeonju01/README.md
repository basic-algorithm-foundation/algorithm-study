# [대소문자 바꿔서 출력하기](https://school.programmers.co.kr/learn/courses/30/lessons/181949)
```java
import java.util.Scanner;

public class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String a = sc.next();
        String answer = "";
        for(int i = 0; i < a.length(); i++) {
            if (a.charAt(i) >= 97 & a.charAt(i) <= 122) {
                answer = answer + Character.toUpperCase(a.charAt(i));
            } else {
                answer = answer + Character.toLowerCase(a.charAt(i));
            }
        }
        System.out.println(answer);

    }
}
```
- char, string, 대소문자 등 문자열 문제를 풀 때 더 쉽고 간단하게 풀 수 있는 방법이 없는지 고민해보기. 아스키코드 기억 안나서 검색해서 해결했다.