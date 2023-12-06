```js
function solution(intStrs, k, s, l) {
  const result = [];
  intStrs.forEach((str) => {
    if (k < Number(str.slice(s, s + l))) {
      result.push(Number(str.slice(s, s + l)));
    }
  });

  return result;
}
```
