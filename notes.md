## 20 string methods in 7 minutes

charAt(#);
- returns the character at specified number
ex. let stringOne = "freeCodeCamp is the best place to learn"
	stringOne.charAt(1)       = r

charCodeAt()
- unicode character from R 

concat()
- joins 2 or more strings and returns a new joined string 
ex. stringOne = "freeCodeCamp"
	stringTwo = "is the best"
	stringOne.concat(stringTwo)           = "freeCodeCamp is the best)

endsWith();
- checks whether a string ends with a specified string or character
ex. let stringOne = "freeCodeCamp is the best place to learn"
	stringOne.endsWith('learn')             = true

includes();
- checks whether a string contains a specified string or character
ex. let stringOne = "freeCodeCamp is the best place to learn"
	stringOne.includes('best')              = true


indexOf();
- returns the position of the first found occurance of a specified value in a string
ex. let stringTwo = "frontend and backend development"
	stringTwo.indexOf('end')                 = 5 because its 5 characters till you hit "end"


lastIndexOf();
- returns the position of the LAST found occurance of a specified value in a string
ex. let stringTwo = "frontend and backend development"
	stringTwo.lastIndexOf('end)              


match();
- search a string against a regular expression and returns the expression in an array
ex. let stringTwo = "frontend and backend development"
stringTwo.match(/end/g)                    = ["end", "end"]


repeat();
- returns a new string with a specified number of copies of an existing string 
ex. let stringTwo = "frontend and backend development"
	stringTwo.repeat(3)                = "frontend and backend developmentfrontend and backend development...etc"


replace();
- searches a string for a specified value or regular expression and returns a new string where the specified values are
ex. let stringTwo = "frontend and backend development"
	stringTwo.replace(/end/g, "END")           
	=== "frontEND and backEND development"


search();
- searches a string for a specified value and returns the position of the match
ex. let stringTwo = "frontend and backend development"
	stringTwo.search("end")                 === 5


slice();
- returns a new array or string where the index is taken out
ex. let stringTwo = "frontend and backend development"
const animals = ['ant', 'bison', 'camel', 'duck', 'elephant'];
	stringTwo.slice(2,4)                   === "frntnd and backend development"
	console.log(animals.slice(2));
// expected output: Array ["camel", "duck", "elephant"]


split();
- split a string into an array of substrings
	- pass in the CHARACTER THAT YOU WANT THE STRING TO BE SPLIT ON
	- (" ") = SPLIT BETWEEN EACH WORD
	- ("") = SPLIT BETWEEN EACH LETTER 


toLowerCase()
- turns an entire string to lowercase letters

toUpperCase()
- turns an entire string to uppercase leters

trim()
- removes "white space" (just regular spaces) in a string






## Common Array methods
arr.push("d")             == pushes "d" into array

pop()
arr.pop()                 == pops last item of array off

concat()
arr.concat(arr2)           == combines 2 arrays into 1

join()
- joins all the elements in a string and doesn't modify the array
- join("!") - will put an ! between every element of an array
ex. arr.join("")                    === "abc"
		arr.join("!")                   === "a!b!c!"


reverse()
- reverses the element order in the array 
- DOES CHANGE THE ARRAY! 


shift()
- removes the first element in the array and returns the element


unshift()
- adds an element to the BEGINNING of the array and returns the array 

slice()
- accepts 2 arguments, the index beginning and index end
- RETURNS A NEW ARRAY 
- arguments - beginning of index, end of index
- ex. arr.slice(1,2)              ["apples", "oranges", "pears"] === ["oranges"]




## Regex 

/([A-Z])\w+/g

[A-Z]        = grab any character uppercase 
()           = match within this set
\w           = grab the letter after it
+            = grab the word after 


^            = matches the beginning of the string 
$            = matches the end of a string 

^a           = matches the beginning of a string with starting letter 'a'




## Slice review
- `if one digit is used (begin isn't defined) => slice begins from index 0`
- `if two digits are used (where to start and where to end) => slice begins at that index # and to the NUMBER BEFORE THE END`
Ex. 
`.slice(1)` ⇒ slice 2nd letter or index (in this case it represents 0) and that is it
`.slice(1,3)` ⇒  slice the 2nd + 3rd character (starting at index 1)