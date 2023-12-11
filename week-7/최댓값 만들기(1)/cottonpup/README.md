```js
function solution(numbers) {
    numbers.sort((a, b) => b - a);
    return numbers[0] * numbers[1];
}
```
- 오름차순으로 정렬하고 가장 높은 숫자들끼리 곱해서 최댓값을 만들면 된다.
