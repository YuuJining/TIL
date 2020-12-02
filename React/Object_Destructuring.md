const human = {
    name: "yujin",
    lastName: "Lee",
    nationality: "Korean",
    favFood: {
        breakfast: "meal",
        lunch: "milk",
        dinner: "bread"
    }
}

const name = human.name;
const lastName = humam.lastName;

console.log(name,lastName); 
-> 효율적이지 않음

const { name, lastName, nationality: difName, favFood: {dinner, breakfast, lunch} } = human;
console.log(name, lastName, difName, dinner, breakfast, lunch);
-> 이렇게 개선할 수 있음 : Object Destructuring