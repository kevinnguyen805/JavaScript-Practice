## Complete the function so that it converts dash-delimited ("kebab" case) & underscore-delimited ("snake" case) words into "camel" casing. 
## The first word within the output should be capitalized only if the original word was capitalized.


function toCamelCase(str){
	let newString = str.replace( /-\w/g, function(beingReplaced){
		return beingReplaced[1].toUpperCase();
	})

	return newString.replace( /_\w/g, function(beingReplaced){
		return beingReplaced[1].toUpperCase();
	})

}

console.log(toCamelCase("the-stealth-warrior"))
console.log(toCamelCase("The_Stealth_Warrior"))

##### Things we learned from this problem

- Essentially - the problem is asking you to split/replace the word for `-` or `_` and then replace the next word
- `you can replace the next character in the index using a function that grabs the letter after -/_ using \w`
- you can also use `.split(/[ _- ]/)` to split the entire word by certain characters



## Write a function called computeUserAverageAge that has a single parameter called users - users is an array of user objects.
function computeUserAverageAge(users){
		let sum = users.reduce(total, num){
			return total + num;
		};
		let average = sum / users.length;
		return Math.round(average);
}


function computeUserAverageAge(users){
	return Math.round((users.reduce( (acc, num) => acc + num.age, 0) / users.length));
}





## How do you add something to the beginning of an array and the end of an array?

Modifies original array ⇒ Mutates the original array, but does not change the reference to it.

- Beginning = unshift() adds item to the beginning of an array
- End = push() adds item to the end of an array

ES6...  ⇒ creates a new array and re-assign an original array, so the new reference is created.

- Beginning = ["item", ...myArray]
- End = [...myArray, "item"]

- Therefore...
    - shift = removes item at beginning of an array
    - pop = removes item at the end of an array


## How do you create a private variable in JavaScript?
function secretVariable(){
	var private = "super secret code";
	return function(){
		return private 
	}
}

let getPrivateVariable = secretVariable();
console.log(getPrivateVariable())                 // "super secret code"
console.log(secretVariable())                     // private



## What is the output?
- must bind the object itself - you cannot place a variable directly on an object key value
     - Because we set it to a new variable, we have to `bind`
     - But `hero.getSecretIdentity()` works by itself because it wasn't **extracted!!!**

let hero = {
	_name: 'John Doe';
	getSecretIdentity: function(){
		return this._name;
	}
}

let stoleSecretIdentity = hero.getSecretIdentity;

console.log(stoleSecretIdentity());               // undefined
console.log(hero.getSecretIdentity());            // John Doe 

OR

// must rebind hero the object - (not just bind the object's key function) 
let stoleSecretIdentity = hero.getSecretIdentity.bind(hero);





## How to capitalize a JavaScript string?
- 