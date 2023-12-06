```js
function solution(my_strings, parts) {
  let result = '';
  parts.forEach((part, i) => {
    const [firstIndex, lastIndex] = part;
    result += my_strings[i].slice(firstIndex, lastIndex + 1);
  });
  return result;
}
```
