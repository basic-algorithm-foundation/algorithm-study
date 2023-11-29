# [9로 나눈 나머지](https://school.programmers.co.kr/learn/courses/30/lessons/181914)
```java
class Solution {
    public int solution(String number) {

        int sumOfAll = 0;
        for(int i = 0; i < number.length(); i++) {
            sumOfAll += Integer.parseInt(Character.toString(number.charAt(i)));
        }

        return sumOfAll % 9;
    }
}
```