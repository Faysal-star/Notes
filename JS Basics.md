# <u>Module 17 : JS Intro & Data Types</u>

```js
//Output
console.log(7);
console.log('Hello World');
console.error('This is error');
console.warn('This is warning');

// Time 
console.time('Hello');
/* some task */
console.timeEnd('Hello'); //prints the run time of tasks
```

```js
//Premitive Data types
var price = 21; //numeric
var name = "Hola" //string
var bools = true; //bolean
var nothing = null; //Null
var symbol = Symbol(); // Symbol Es6

//Reference Types - objects 
const array = ['movies' , 'music'];
const menu = {
    item : 'Mashed Potato' ,
    price : 200 ,    
}

//typeof

console.log(typeof price);
console.log(typeof name);
console.log(typeof bools);

//date
var today =  new Date();
console.log(typeof today); //object
console.log(today);
```

```js
//Mathematical Operations
var price = 12;
var price2 = 13;
var total = price m+ price2 ; // +,-,*,/,%

console.log(total);
console.log(price + price2);


price += 10 ; // += , -= , *= , /= , ++ , --

/* Math Objects */
let maths
maths = Math.PI ; 
maths = Math.E ;
maths = Math.round(2.4); //2
maths = Math.ceil(2.6); //3
maths = Math.floor(2.6); //2
maths = Math.sqrt(64); //8
maths = Math.abs(-3); //3
maths = Math.pow(8 , 2); //64
maths = Math.min(2,3,4,6,-2); //-2
maths = Math.max(2,33,-1,4,15); //33
maths = Math.random();
maths = Math.floor(Math.random()*10 + 1); //random(1,10)
```

```js
//Type Conversion
var firstName = 'Faysal';
var lastName = 'Mahmud';
var fullName = firstName + ' ' + last ; //Concatenation

console.log(fullName);
console.log(fullName.length);

var price = '42.5';
var floatPrice = parseFloat(price);
var intPrice = parseInt(price);


var prices = 0.100003;
// prices = total.toFixed(1);
// prices = parseFloat(total);
console.log(parseFloat(prices.toFixed(1)));
```

```js
//let 
let name = 'Faysal'; //same as var
name = 'Mahmud';
console.log(name); //Mahmud

//const
const PI = 3.14 ; //can't be reassign 
```

```js
//Array
let array = [1,2,3,4];
array.push(5);


console.log(array); //[1,2,3,4,5]


//Object 

let object_list = {a:1, b:2, c:3};
console.log(object_list); 
console.table(object_list); //print table
```

```js
//Type conversion all
let test;
//Number to string
test = String(555);
//Bool to string
test = String(true);
//date to string
test = String(new Date());
//Array to string
test = String([1,2,3,4]);

/* toString() */
test = (5).toString();


/* String to Number */
test = Number('5'); //5
test = Number(true); //1
test = Number(false); //0
test = Number('hola'); //NaN -> Not a Number
test = parseInt('5.6'); //5
test = parseFloat('5.6') //5.6
```

**<u>String</u>**

```js
let val ;
let sentence;

// Concatenation 
var firstName = 'Faysal';
var lastName = 'Mahmud';
let age = 20 ;
var fullName = firstName + ' ' + last ; // Faysal Mahmud
// Concate 
fullName = firstName.concat(' ', lastName);

// Append
fullName += 'Kishore' //Faysal Mahmud Kishore
sentence = 'Hello, I am '+ fullName + ' and I am ' + age ;

// Escaping 
sentence = 'That\'s awesome , I cant\' wait';


// Change case
val = firstName.toUpperCase(); //FAYSAL
val = firstName.toLowerCase(); //faysal


// index

val = firstName[0]; // F
val = firstName.indexOf('y'); // 2
val = firstName.lastIndexOf('y'); //3


// charAt
val = firstName.charAt(0); //F
/* last char */
val = firstName.charAt(firstName.length - 1); //l


// Substring
val = firstName.substring(0,4); //Fays

// slice
val = firstName.slice(0,4); //Fays
val = firstName.slice(-3); //sal

// Split
let str = "Hola to my friends";
val = str.split(' '); // ['Hola','to','my','friends']


// Replace
val = str.replace('my' , 'Your'); // Hola to Your friends

// includes
val = str.includes('to'); //true
val = str.includes('too'); //false
```

Template Literals

```js
// Es6 Template Strings
var firstName = 'Faysal';
var lastName = 'Mahmud';
let age = 20 ;
let html ;

html =`
    <ul>
     <li>First : ${firstName}</li>
     <li>Last : ${lastName}</li>
     <li>Age : ${age}</li>
     <li>${age > 19 ? 'Not Teen' : 'Teen'}</li>
    </ul>`;
document.body.innerHTML = html ;
```

Array

```js
//Array
const numbers = [1,2,3,4,5];
const numbers2 = [6,7,8];
const fruit = ['am','jam'.'kathal']
let val;
//length
val = numbers.length; // 5
// check if is array
val = Array.isArray(numbers); //true
// Get single value
val = numbers[2]; // 3
// edit or insert into array
numbers[2] = 5 ;
// Find index
val = fruit.indexOf('jam'); //1

// Mutating array

// Add last
numbers.push(6);
// remove last
numbers.pop();
let poped_item = numbers.pop(); //5
// Add first
numbers.unshift(12);
// remove fist
numbers.shift();
// Splice values
numbers.splice(1,3); // splice(start, remove after that)

// COncatenate array
val = numbers.concat(numbers2); // add two array
// SOrting
val = fruit.sort(); //workd for string

//check if is in array 
if(fruit.indexOf('peyara') == -1){ console.log('peyara nai ') ;}
else if(fruit.indexOf('peyara') != -1){console.log('peyara ache') ;}

// Number sorting
// Assending 
val = numbers.sort(function(x,y){
    return x - y ;
});
// Descending 
val = numbers.sort(function(x,y){
    return y - x ;
});

// Find
```

Object Literals

```js
const person = {
    first : 'Faysal',
    last : 'Mahmud',
    age : 19,
}

let val ;
// Get full
val = person ;

//Get specific
val = person.first ;

//change value
person.age = 20 ;
person['age'] = 21;

val = person.age ;
person[val] = 22 ;

// Array
```

Dates & Times

```js
let val ;

const today = new Date();

let birthday = new Date('3-14-2001 10:25:00');
birthday = new Date('March 14 2001');
birthday = new Date('3/14/2001');


val = today.getMonth();
val = today.getDate();
val = today.getDay();
val = today.getFullYear();
val = today.getHours();
val = today.getMinutes();
val = today.getSeconds();
val = today.getMilliseconds();
val = today.getTime();

birthday.setMonth(1);
birthday.setDate(15);
birthday.setFullYear(2002);
```

If - Else

```js
// Condition
const color = 'red' ;
if(color == 'red'){
    consol.log('red');
}
else if(color == 'green'){
    console.log('green');
}
else{
    console.log('no color');
}
```

Switch

```js
const color = 'red';
switch(color){
    case 'red':
        console.log('color is red');
        break;
    case 'blue':
        console.log('Color is blue');
        break;
    default :
        console.log('Muri');
        break;
}
```

Function

```js
function greet(name){
    return 'hello' + name;
}
console.log(greet('Faysal'));

// Function Expressions
const square = function(x){
    return x*x;
};
console.log(square(9));

// Immidiately Invokable Dunction Espressions - IIFes
(function(){
    console.log('Hola');
})();


(function(name){
    console.log('Hola' + name );
})('Faysal'); /* Hola Faysal */


// Property Mehod

//in object
const todo ={
    add: function(){
    console.log('add todo');
    },
    edit : function(id){
    console.log("Edit $(id)");
    }
}
//adding to object
todo.delete = function(){
    console.log('Delete');
}
//calling values
todo.add();
todo.edit(22);
todo.delete();
```

Loop

```js
//for loop

for(let i = 0 ; i < 10 ; i++){

    if(i == 2){
        console.log('2 is my fav');
        continue;
    }
    if(i == 5){
    break;
    }
    console.log(i);

}

// While 
let i = 0;
while(i < 10){
    console.log(i);
    i++;
}

// Do While
let i = 0 ;

do{
    console.log(i);
    i++;
}
while(i < 10); 

// forEach
const fruits = ['am','jam'.'kathal'];

fruits.forEach(function(fruit){
    console.log(fruit);
});

//Map
const users = [
    {id : 1 , name:'a'},
    {id : 2 , name:'b'},
    {id : 3 , name:'c'},
];

const ids = users.map(function(user){
    return user.id;
});
console.log(ids);

// For in loop 
const user = {
  firstName: 'John', 
  lastName: 'Doe',
  age: 40
}

for(let x in user){
  console.log(`${x} : ${user[x]}`);
}
```

 Alerts 

```js
// Alert
alert('hello');

// Prompt
const input = prompt();
alert(input);

// Confirm
if(confirm('Are you sure')){
    console.log('Yes');
}
else{
    console.log('No');
}

let val;
// Outer height and width
val = window.outerHeight;
val = window.outerWidth;
// Inner height and width
val = window.innerHeight;
val = window.innerWidth;

// Scroll Points
val = window.scrollY;
val = window.scrollX;

// Location
val = window.location;


// History Object
window.history.go(-1);

// Navigator
val = window.navigator;
```
