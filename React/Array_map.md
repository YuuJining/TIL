const days = ["Mon", "Tues", "Thurs", "Fri"];

> 예시1
const smilingDays = days.map(potato => console.log(potato));
-> days에 있는 모든 요일에 function 실행
-> Mon Thues Thurs Fri 출력되지만,
빈 배열이 return됨
-> map은 각각의 Function의 결과 값으로 배열을 return해 줌

이렇게 개선...

const smilingDays = days.map(potato => `★ ${potato}` );
console.log(smilingDays);
-> ["★ Mon", "★ Tues", "★ Thurs", "★ Fri"] 출력

> 예시2
const smilingDays = days.map((day, index) => `#${index + 1} ${day}`);
-> ["#1 Mon", "#2 Tues", "#3 Thurs", "#4 Fri"] 출력