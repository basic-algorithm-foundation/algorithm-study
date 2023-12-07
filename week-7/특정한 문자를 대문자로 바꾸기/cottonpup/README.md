```js
function solution(my_string, alp) {
    let result = "";
    for (let i = 0; i < my_string.length; i++) {
        if (my_string[i] === alp) {
            result += my_string[i].toUpperCase();
        } else {
            result += my_string[i];
        }
    }
    return result;
}
```
- 자바스크립트에서의 문자열은 불변
