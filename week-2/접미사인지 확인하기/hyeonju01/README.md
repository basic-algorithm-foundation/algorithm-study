# [접미사인지 확인하기](https://school.programmers.co.kr/learn/courses/30/lessons/181908)
```java
class Solution {
    public int solution(String my_string, String is_suffix) {
        int answer = 0;
        String[] suffixes = new String[my_string.length()];
        int e = my_string.length();

        for (int i = 0; i < my_string.length(); i++) {

            String suffix = my_string.substring(i, e);
            suffixes[i] = suffix;

        }

        for (String word : suffixes) {
            if (word.equals(is_suffix)) {
                answer = 1;
            }
        }

        return answer;
    }
}
```