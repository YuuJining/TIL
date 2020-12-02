## arrow function은 return을 한다는 것이 함축되어 있다. -> 중괄호를 하지 않으면 return

## argument가 하나라면 괄호를 할 필요 없음. 두 개 이상이라면 괄호가 필요함.

>예시1
const sayHello = (name) => "Hello" + name;
const yujin = sayHello("yujin");
console.log(yujin);

const sayHello = (name = "Human") => "Hello " + name;
-> 이 경우는 default값으로 Human을 준 경우임


>예시2 - event 처리
const button = document.querySelctor("button");

const handleClick = event => console.log(event);

button.addEventListener("click", handleClick);

혹은

button.addEventListener("click", event => console.log(event));