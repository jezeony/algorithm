# qr code

## 문제 링크

https://school.programmers.co.kr/learn/courses/30/lessons/181903
<br>

## 나의 풀이

```js
function solution(q, r, code) {
    const arr = [];
    for(i=0; i < code.length; i++){
       if(i % q === r) arr.push(code[i])
   }
    
    return arr.join("");
}
```
<br>

## 다른 풀이
- 문자열의 각 인덱스로 배열 만드는 방법 : [...문자열]
```js
function solution(q, r, code) {
  return [...code].filter((_, i) => i % q === r).join('');
}
```