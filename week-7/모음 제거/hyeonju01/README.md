# []()
### 틀린 답
```java
class Solution {
    public String solution(String my_string) {
        String answer = "";
        String original = my_string;
        StringBuffer sb = new StringBuffer(my_string);
        String[] vowel = {"a", "e", "i", "o", "u" };
        
        for(int i = 0; i < original.length(); i++){
            String temp = Character.toString(original.charAt(i));
            for(int j = 0; j < vowel.length; j++) {
                if (temp.equals(vowel[j])) {
                    sb.deleteCharAt(i);
                }
            }
        }
        
        return sb.toString();
    }
}
```

```java
import java.util.ArrayList;

class Solution {
    public String solution(String my_string) {
        String answer = "";
        ArrayList<String> notVowels = new ArrayList<>();
        
        String[] vowel = {"a", "e", "i", "o", "u" };
        
        for(int i = 0; i < my_string.length(); i++){
            String temp = Character.toString(my_string.charAt(i));
            for(int j = 0; j < vowel.length; j++) {
                if (!temp.equals(vowel[j])) {
                    notVowels.add(temp);
                }
            }
        }
        
        return String.join("", notVowels);
    }
}
```

### 맞은 답
```java
import java.util.*;

class Solution {
    public String solution(String my_string) {
        String answer = "";
        ArrayList<String> notVowels = new ArrayList<>();
        
        ArrayList<String> vowel = new ArrayList<>(List.of("a", "e", "i", "o", "u"));
        
        for(int i = 0; i < my_string.length(); i++){
            String temp = Character.toString(my_string.charAt(i));
            if (!vowel.contains(temp)) {
                notVowels.add(temp);    
            }
        }
        
        return String.join("", notVowels);
    }
}
```

- 알게 된 것 
List.contains() : 파라미터가 리스트에 존재하면 true, 없으면 false를 반환한다.  