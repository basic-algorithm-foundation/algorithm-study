```js
function solution(numbers, direction) {
    const trimmedNumbers = numbers;
    if(direction === 'right'){
      trimmedNumbers.unshift(numbers[numbers.length - 1])
      trimmedNumbers.pop();
    } else {
        trimmedNumbers.push(numbers[0])
        trimmedNumbers.shift();
    }
    
    return trimmedNumbers;
}
```
- `unshift`와 `shift`, `pop` 메서드에 대해서 다시 공부
