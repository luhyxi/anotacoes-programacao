
---
# Planning
## Objectives:
- 


## Goals:
- 
- 
- 

# Definition:


# Technologies:



# Notes:

#### Em frontend:
Modifica os elementos de um [[HTML and CSS]] através de um arquivo externo ou através de um script interno no [[HTML and CSS]]

# Stuff:
#### Inserção em HTML
```html 
...
<body>
	<script src="aPorradoJavascript.js"></script>
</body>
```
#### Códigos em js:
```javascript
//Print em javascript:
console.log

// lib math 
var x
math.x()

//Estr. d/ resp. dif
do{
	...;
} while(...)

for (x in y){
...
}


//Estr. Switch
switch(x){
	case 0:
	...
	default:
	...
}
```

```javascript
// FORMAS DE CHARMAR FUNÇÕES NO JAVASCRIPT!!!


// Constructor
const multiply = new Function("x", "y", "return x * y");

// Declaration
function multiply(x, y) {
  return x * y;
} // No need for semicolon here

// Expression; the function is anonymous but assigned to a variable
const multiply = function (x, y) {
  return x * y;
};
// Expression; the function has its own name
const multiply = function funcName(x, y) {
  return x * y;
};

// Arrow function
const multiply = (x, y) => x * y;

// Method
const obj = {
  multiply(x, y) {
    return x * y;
  },
};
```

## Functions in JS:
- They are called by ref

	- Reg Func. -> Returns anything
	- Async Func. -> Returns _promisse_ with pause and resume _await_
	- Gen Func. -> Returns _generator_ with pause and resume _yield_
	- Async Gen. Func. -> Returns _async generator_ with pause and resume _await_ and _yield_

### [[Arrowfunctions]] in JS:

```javascript
() => expression

param => expression

(param) => expression

(param1, paramN) => expression

() => {
  statements
}

param => {
  statements
}

(param1, paramN) => {
  statements
}

// Traditional Function
function bob(a) {
  return a + 100;
}

// Arrow Function
const bob2 = (a) => a + 100;
```

## Datatypes:
#### List:
push -> add elem. to array
list.length -> retorna a len de um elemento ou de toda lista
splice(pos,0/1,nov_elem)-> add nov_elem em pos
	0 -> preserva elems em posição
	1 -> remove elems em posição
.pop -> remov. elem. final
.shift -> manda elem[1] para [0]
x.length = 4 (remoção por length)
.splice(x,y) remove x até y


---
### Sources: 

### Related Resources: 


