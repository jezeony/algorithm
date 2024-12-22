# OX퀴즈

## 문제 링크

https://school.programmers.co.kr/learn/courses/30/lessons/120907
<br>

## 나의 풀이

```js
	function solution(quiz) {
		const answer = [];

		quiz.map((str) => {
			const arr = str.split(" ");

			if (arr[1] === "+") {
				Number(arr[0]) + Number(arr[2]) === Number(arr[4]) ? answer.push("O") : answer.push("X");
			}

			if (arr[1] === "-") {
				Number(arr[0]) - Number(arr[2]) === Number(arr[4]) ? answer.push("O") : answer.push("X");
			}
		});
		
		return answer;
	}
```
<br>

## 다른 풀이
- 구조분해 할당 사용
```js
function solution(quiz) {
    let answer = [];
    
    quiz.forEach((val) => {
        const [x, sign, y, , z] = val.split(" ");
        
        let sum = 0;
       
       if (sign === "+") {
            sum = Number(x) + Number(y);
        } else {
            sum = Number(x) - Number(y);
        }
        sum === Number(z) ? answer.push("O") : answer.push("X");
    });
    
    return answer;
}
```