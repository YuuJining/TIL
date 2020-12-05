# forEach - 각각의 대해서~

let posts = ["Hi","Hello","Bye"];

posts.forEach(post => console.log(post))
-> map, filter는 배열을 return하지만 forEach는 각각의 아이템에 대해서 어떠한 시행을 함.

posts.push("good");
-> push는 새로운 아이템을 배열에 추가함

if(!posts.includes("Hi")) {
    posts.push("Hi");
}
->posts에 Hi가 없으면 Hi 추가 