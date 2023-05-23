# Section 2: 자바스크립트 새로고침

## 11. 모듈소개
    보통 가장 최신 버전의 자바스크립트와 차세대 기능을 사용해서 깔끔하고 강력한 리액트 입을
    작성할 수 있게 해주고 리앵긑 자체가 수많은 자바스크립트 기능을 사용하기 떄문이다.

    앞으로 우리가 사용하 핵심 기능들을 살펴볼 것이고, 이후에 여러분들은 그런 코드에 익숙해지기 바란다.

## 12. let과 const

### 변수 생성 종류
1. var
2. let
3. const

let, const을 사용 권장

let은 값을 수정할 수 있는 변수를 선언할 때 사용
const는 한 번 지정하면 절대 변화지 않는 값인 상수를 선언할 때

## 13. 화살표함수(Arrow fucntions)
장점 : this 라는 키워드 이슈를 해결 해준다.

화살표 함수 안에 이 this를 사용하면, 항상 정의한 객체를 나타내고, 실행 중에 갑자기 바뀌지 않을 것임.

받을 인수가 2개 이상일 경우

기존에 함수
```
function  printMyName(name, age) {
  console.log(name, age);
} 

printMyName('kim',28);
```

화살표 함수 적용
```
const printMyName = (name, age) => {
  console.log(name, age);
}

printMyName('kim',28);
```

받을 인수가 한 개인 경우
```
const multiply = number => number * 2;
 
console.log(multiply(2));
```

1개 혹은 그 이상의 인수를 취해서 값을 반환하는 함수를 작성하고 아주 짧고 함축적인 방법임

## 14. Export 와 Imports

### default Export
```

예시
import person from './person.js'
import prs from './person.js'

두 개의 다른 상수를 불러오는데 그 파일에서 특정한 어떤 것을 정확하게 기리키기 위해 export 구문에 중괄호`{}`를 사용
이것을 named export라고 함. 이름으로 어떤것을 부럴오기 때문입니다.
그래서 우리가 가리키는 것을 정확하게 자바스크립트가 알게 하려면 정확한 이름을 중괄호 사이에 입력해야 합니다
```

### name export

```
예시
import {smth} from './utility.js'
import {smth as Smth} from './utility.js'
import * as bundled from './utility.js' // 전체 js 호출

그리고 import문에 콤마를 넣어서 {baseData,clean} 또는 {clean, baseData} 라고 한 문장으로 함
```

## 15. Classes (객체 생성)
```
    class Person {
        name = 'Max' // 프로퍼티 : 클래스에 정의한 변수
        call = () => {} // 메소드 : 클래스에 정의한 함수
    }

    new 키워드로 생성(좀 더 편한 방법임)
    const myPerson = new Person()
    myPerson.call()
    console.log(myPerson.name)

    클래스 상속
    class Person extends Master
```

```
예시
class Human {
  constructor() {
    this.gender = 'male';
  }
  printGender() {
    console.log(this.gender);
  }
}


class Person extends Human {
  constructor() {
    super();
    this.name = 'kim'
  }
  
  printMyName() {
    console.log(this.name)
  }
  
}

const person = new Person();
person.printMyName(); // "kim"
person.printGender() // "male"
```

## 16. 클래스, 속성 및 메서드
1. 프로퍼티 : 클래스와 객체에 추가되는 변수
2. 메소드 : 클래스와 객체에 추가되는 함수 같은 것
3. this구문 : 프로퍼티와 생성자함수를 설정하는 것

```
메소드는 : 값으로 함수를 저장하는 프로퍼티
myMethod = () => {}
프로퍼티 값으로 화살표 함수를 사용하기 때문에 this 키워드를 사용하지 않아도 됨.

class Human {
   gender = 'male';

  printGender = () => {
    console.log(this.gender);
  }
}


class Person extends Human {
    name = 'kim'
    gender = 'female';
  
  printMyName() {
    console.log(this.name)
  }
  
}

ex
class Human {
   gender = 'male';

  printGender = () => {
    console.log(this.gender);
  }
}

ex
class Person extends Human {
    name = 'kim'
    gender = 'female';
  
  printMyName() {
    console.log(this.name)
  }
}

const person = new Person();
person.printMyName(); // kim
person.printGender() // female
```

## 17. 스프레드 및 연산자
`...`인 연산자임
어디에 사용하는지에 따라 스프레드 or 레스트

스프레드 연산자
1. 배열의 원소나 객체의 프로퍼티를 나눈다.
2. 원래 기존에 있는 객체에서 새로운 객체로 덮여쓰여지는 것이다.
3. 우리가 갖고 있는 프로퍼티가 우선권을 갖습니다.
4. 앞에 미리 나온 객체를 취해서 새로운 객체에 전달을 한다.

레스트 연산자
1. 함수의 인수 목록을 배열로 합치는데 사용
```
예시
```
// ... 연산자를 사용하지 않을 경우
const numbers = [1, 2, 3];
const newNumbers = [numbers, 4];

console.log(newNumbers) // [[1, 2, 3], 4]

// ... 연산자를 사용한 경우
const numbers = [1, 2, 3];
const newNumbers = [numbers, 4];

console.log(newNumbers) // [1, 2, 3, 4]


스프레스 연산자

const person = {
  name: 'kim'
};

const newPerson = {
  ...person,
  age : 28
}

console.log(newPerson)

[object Object] {
  age: 28,
  name: "kim"
}

const filter = (...args) => {
  return args.filter(el => el === 1);
}
```
console.log(filter(1, 2, 3)) // [1]
```

## 18 구조분해할당(Destructuring)
- 배열의 원소나 객체의 프로퍼티를 추출해서 변수에 저장할 수 있도록 해주는 것
- 원소나 프로퍼티를 하나만 가져와서 변수에 저장

### 사용 목적
- 배열에서 특정 원소나 객체에서 특정 속성을 추출하는 편한 방법이 있다.

```
const numbers = [1, 2, 3];
[num1, ,num3] = numbers;
console.log(num1,num3) // 1,3
```
왼쪽에서 중괄호를 사용하여 속성 이름을 사용하여 속성을 대상으로 지정하는 구문이다.

## 18  참조형 및 원시형 데이터 타입

### 기본형 타입
- 숫자(number)
- 문자(string)
- 벌룬(boolean)

### 특징

- 재할당하거나 변수를 다른 변수를 다른 변수에 저장할 때, 값을 복사합니다.

```
const number = 1;
const num2 = number;

console.log(num2) // 1
```

### 참조형 자료 타입
- 객체(Object)
- 배열(Array)

```
const person = {
  name : 'Max'
};

const secondPerson = person;

person.name = 'Manu'; 

console.log(secondPerson)

// [object Object] {
//  name: "Manu"
// }


const person = {
  name : 'Max'
};

const secondPerson = {
  ...person
}

person.name = 'Manu';

console.log(secondPerson)

// [object Object] {
//  name: "Max"
// }


```
객체의 요소 바꾸면 객체의 있는 name도 같이 바꾸어짐(배열도 마찬 가치임)

리액트에서는 실수로 앱의 다른 주소에 있는 같은 객체로 다르게 사용하도록 조작할 수도 있습니다.
스프렌드 연산자를 사용을 할 수 있다.


## 20. 배열 함수 새로 고침

### map() 함수
-  기존의 값을 새 값으로 반환합니다.

```
const numbers = [1, 2, 3];

const doubleNumArray = numbers.map((num)=> {
    return num * 2;
});

console.log(numbers); // [1, 2, 3]
console.log(doubleNumArray); // [2, 4, 6]
```
이전의 배열은 바뀌지 않았고 새 배열의 원소들은 값이 두 배가 된 것을 볼수 있다.

## 21. 마무리






