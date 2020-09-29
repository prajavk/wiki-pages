# Javascript Coding


1. How to use bind() feature in javascript with this example?

```
let button = function(content) {
 this.content = content;
};

button.prototype.click = function() {
 console.log(`${this.content} clicked `);
};

Ans:
let newbtn = new button('add');

let boundclick = newbtn.click.bind(newbtn);
boundclick();
```

2. How to use bind() in async fun()

```
let myobj = {
 asyncGet(cb) {
  cb();
 },
 parse() {
  console.log('parse called');
 },
 render() {
  this.asyncGet(function() {
   this.parse();
  }.bind(this))
 }
};
myobj.render();
```

3. Is below Array valid and called as?

```
var myArray = [
 [
  []
 ]
];

A. 3 dimension array
````

4. What value is returned from the above statement?

```
var test = "i'm a lasagna hog".split("").reverse().join("");

A: "goh angasal a m'i"
```

5. Which value is returned?

``` 
(function(x) {
 delete x;
 return x;
})(1);
```
6. What is the outcome of the two alerts?

```
var foo = "Hello";
(function() {
 var bar = " World";
 alert(foo + bar);
})();
alert(foo + bar);

A: "Hello World" & ReferenceError: bar is not defined
```

7. What is the value of foo.length?

```
var ninja = {};
ninja.bar = 'hello';

Ans: undefined
```
8. what is the value of "x"?

```
var y = 1,
 x = y = typeof x;
x;
```

9. Consider the two functions below. Will they both return the same thing? Why or why not?

```
function foo1() {
 return {
  bar: "hello"
 };
}

function foo2() {
 return {
  bar: "hello"
 };
}
```

10. Will this function allow an arbitrary number of arguments? Print console by reading arguments.

```
sum(2, 3);
sum(1, 2, 3, 4);

Ans.
function sum() {
 for (var i = 0; i < arguments.length; i++) {
  console.log(arguments[i]);
 }
}
```
11. what will be printed in ES5?

```
function calculateTotalAmount(vip) {
 var amount = 0
 if (vip) {
  var amount = 1
 } { // more crazy blocks!
  var amount = 100 {
   var amount = 1000
  }
 }
 return amount
}
console.log(calculateTotalAmount(true));
```

12. Using ES6, refactor this code to perform Parallel tasks(without error handling)?

```
// This is sequential tasks (without error handling)
function getTotalFileSize(file1, file2, fil3, callback) {
 let total = 0;
 stat(file1(error, info) => {
  total += info.size;
  stat(file2(error, info) => {
   total += info.size;
   stat(file3(error, info) => {
    total += info.size;
    callback(total);
   });
  });
 });
}
```

13. Does this code work?

```
function hello(track) {
 if (track === 'skill') {
  action = 'dance';
 } else {
  action = 'skip';
 }
 var action;

 return action;
}
```

14. Explain why the following doesn't work as an IIFE: Immediately invoked function expression. will there be any error in the code?

```
function foo(){
 // your logic here
}();

Ans: functions as expressions vs definitions.
// To fix this bug, write like:
( function foo() {}) ();
```

15. which will print?

```
var x = 1;
var y = true;
if(x===y){
    console.log('Equals');
}else{
    console.log('Not Equals');
}
```
16. which will print?

```
var a = 0;
console.log(typeof a);
if(typeof a !='undefined'){
  console.log('Exist');
}else{
    console.log('Not Exist');
}
```
17. which will print?

```
var my = 10;
function func() {
    my = 25;    
    var my;
}
func();
console.log('var=' , my);
```
18. Fun() declaration vs Fun expression

```
expression(); // givs error - expression undefined?

myfun();

var expression = function() {
    console.log('hi from my expression');   
}

function myfun(){
    console.log('hi from myfun');
}
```
19. which print first? 

```
var xx = 5;
// func declaration
function print(input) {
    var xx = 0; 
    function log(){
        // inside fun
    }    
    console.log(input, xx); // prints 10, 0
}
print(10);
```

20. when var is null, undeclared, undefined?

```
// undefined
let foo;
let bar = {};
let baz = ['jon', 'phil', 'ed'];
const qux = function(){	
};
console.log(foo,bar.name, baz[4], qux());

// How to check for undefined?
console.log(typeof foo, typeof bar);
console.log(foo === undefined); //  gives true 
const baz = 'undefined';
console.log(baz === undefined); // false

const come = null;
console.log(come); // null
```

21. Find bug in this script? 

```
let foo; // undefined
const bar = null; // null
// compare both
console.log(foo == bar); true?
```

22. Javascript control variable scope?

```
( function foo() {}) (); 
console.log(foo);

Ans: Firefox - referenceError: foo is not defined
```
23. what is the printed in ES5?

```
function calculateTotalAmount(vip) {
	var amount = 0
	if (vip) {
		var amount = 1
	} { // more crazy blocks!
		var amount = 100 {
	        var amount = 1000
		}
	}
	return amount
}
console.log(calculateTotalAmount(true));
```

24. Consider two functions as below. Will they both return the same thing? Why or why not?

```
function foo1() {
	return {
		bar: "hello"
	};
}
function foo2() {
	return {
		bar: "hello"
	};
}
```
25. Using ES6, refactor this code to perform Parallel tasks(without error handling)?

```
// sequential tasks (without error handling)
function getTotalFileSize(file1, file2, fil3, callback) {
	let total = 0;
	stat(file1(error, info) => {
		total += info.size;
		stat(file2(error, info) => {
			total += info.size;
			stat(file3(error, info) => {
		total += info.size;
		callback(total);
			});
		});
	});
}
```
26. Does this code works?

```
function hello(track) {
	if (track === 'skill') {
		action = 'dance';
	} else {
		action = 'skip';
	}
	var action;

	return action;
}
```






