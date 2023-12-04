```js
function solution(l, r) {
    const result = [];
    for (let i = l; i <= r; i++) {
        let numStr = i.toString();
        let isValid = true;
        for (let char of numStr) {
            if (char !== '0' && char !== '5') {
                isValid = false;
                break;
            }
        }
        if (isValid) {
            result.push(i);
        }
    }
    return result.length > 0 ? result : [-1];
}

```
- 챗지피티 도움을 받았다.
- string 은 for .. of 문 순회 제발 잊지 말자!
- 값이 '0' 이거나 '5' 인 경우로 풀으니까 15와 같은 경우도 조건식을 만족했다. 값이 '0'이거나 '5'가 아닌경우로 조건을 작성했다면 좋았을텐데 아쉬움이 느껴진다. 

```js
function solution(l, r) {
    const result = [];
    for (let i = l; i <= r; i++) {
        if (/^[0|5]+$/.test(i.toString())) {
            result.push(i);
        }
    }
    return result.length > 0 ? result : [-1];
}
```
- 챗지피티 도움을 받았다.
- regex 정규표현식을 혼자 잘 작성하면 좋겠지만 코테보면서 작성하기는 어려움이 많을 거 같다. 따라서 이 식은 참고만 하자.
- 정규 표현식 `/^[0|5]+$/` 에 대하여
   - `^`: 이 기호는 문자열의 시작 부분
  - `[0|5]`: 대괄호 []는 문자 집합
  - `$`: 이 기호는 문자열의 끝 부분