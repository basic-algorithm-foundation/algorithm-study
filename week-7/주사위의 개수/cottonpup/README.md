```js
function solution(box, n) {
  const widthFit = Math.floor(box[0] / n);
  const lengthFit = Math.floor(box[1] / n);
  const heightFit = Math.floor(box[2] / n);

  return widthFit * lengthFit * heightFit;
}
```
- 깊게 생각할 필요없이 그냥 양변들을 나누고 곱해버리면 됐다. 수학에 약하니까 잘 기억해두면 하는 문제!
