# Programming -> Functional Programming / Object-Oriented Programming

>예시
class Human {
    constructor(name, lastName) {
        this.name = name;
        this.lastName = lastName;
    }
}

class Baby extends Human {
    cry() {
        console.log("Waaaaa");
    }
}

const mBaby = new Baby("mini", "kim");

const yujin = new Human("yujin","lee");
