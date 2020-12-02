>예시1
const days = ["Mon", "Tues", "Wed"];
const otherDays = ["Thu", "Fri", "Sat"];

const allDays = [...days, ...otherDays, "Sun"];

console.log(allDays);

=> ["Mon", "Tues", "Wed", "Thu", "Fri", "Sat", "Sun"] 으로 출력됨

>예시2
const ob = {
    first: "hi",
    second: "hello"
}

const ab = {
    third: "bye"
}

const two = {ob, ab};
console.log(two); -> 이렇게만 출력하게 되면 두 Object가 있는 하나의 Object가 나옴

const tow = {...ob, ...ab};
-> spread operator 사용하기
