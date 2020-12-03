## filter method
#### 주어진 Function을 통과한 모든 원소들로 이루어진 배열을 생성하는 함수임


### map Function은 배열의 모든 Argument에 Function을 실행하고 그 결과 값들로 이루어진 배열을 생성하지만
### filter Function은 배열의 모든 요소들에 Function을 실행해서 true를 return하는 요소로만 이루어진 배열을 만듦

> 예시1
const numbers = [1, 3, 45, 14, 67, 8, 35, 23, 55, 68];

const biggerThanFifth = numbers.filter(number => number > 15);

> 예시2
let posts = ["Hi", "Hello", "Bye"];
posts = posts.filter(post => post !== "Bye");
-> Hi, Hello로 구성된 배열 return


