# Code reading

## Question 1

Take a look at the following code:

```
1    let x = 1;
2    function f1()
3    {
4        let x = 2;
5        console.log(x);
6    }
7    console.log(x);
```

Explain why line 4 and line 6 output different numbers.

line 5 output will execute line 4 (local scope) and line 7 execute global scope variable

## Question 2

Take a look at the following code:

```
let x = 10

function f1()
{
    console.log(x) 
    let y = 20
}

console.log(f1()) // will execute line 30 and the output will be 10
console.log(y) // ReferenceError y is not defined / y is in local scope
```

What will be the output of this code. Explain your answer in 50 words or less.

## Question 3

Take a look at the following code:

```
const x = 9;

function f1(val) {
  val = val + 1;
  return val;
}

f1(x); // this funcation is called but it can not change the x value;
console.log(x); // the output of this line is 9 (Global scope line 45)

const y = { x: 9 };

function f2(val) {
  val.x = val.x + 1;
  return val;
}

f2(y);
console.log(y); // the output will be { x: 10 } because line 55 is an object and in line 58 changed the value of x and not y.
```

What will be the output of this code. Explain your answer in 50 words or less.
