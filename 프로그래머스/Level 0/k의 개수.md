# k의 개수

## 문제 링크

https://school.programmers.co.kr/learn/courses/30/lessons/120887
<br>

## 나의 풀이

```js
function solution(i, j, k) {
    let count = 0;
    
    for(i=i; i<=j; i++){
       count += String(i).split('').filter(el => el===String(k)).length;
    }
    
    return count;
}
```

## 다른 풀이

```js
function solution(i, j, k) {
    let a ='';
    
    for(i;i<=j;i++){
        a += i;
    }

    return a.split(k).length-1;
}
```
