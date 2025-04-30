## Part 2
1. On line 12, the variable value for *i* will be printed due to the fact that the variable was declared using ```var```. As we have previously stated that ```var``` variables persist past their scopes and act as global variables, which can be accessed in unexpected places. In this case, the variable *i* was declared as an iterator of the for loop. But the variable persists due to the nature of ```var``` and when called in a ```console.log``` statement will print the length of the prices (3).
2. On line 13, the variable value for *discountedPrice* will be printed due to a same logic in question #1. Because the variable was declared using ```var```, the variable will persist past its scope and when called on, will print: "150"
3. On line 14, following the same logic as question #1 and #2, the *finalPrice* variable is declared with ```var```. However, regardless whether it was declared with ```let``` or ```var``` this variable will still be able to be accessed due to the fact that we are still in the scope it was declared in. Line 14 will print: "150" (```Math.round(150 * 100) /100```)
4. The function will return the variable *discounted*. There will be no error in this function return statement. The return statement is simply returning the variable from the function. Since the discounted variable was declared within the scope of the function, there will be no error in returning its value. The function will return the following:
   1. ```discounted = [50, 100, 150]```
5. An error will occur when line 12 is run because the statement is trying to access a variable that does not exist outside the for loop. The variable *i* is declared with ```let``` and therefore will not persist outside of its delaration scope. In summary, the ```console.log``` statement will return an error.
6. An error will occur when line 13 is run because the statement is trying to access a variable that does not exist outside the for loop. The variable *discountedPrice* is declared with ```let``` and therefore will not persist outside of its delaration scope. In summary, the ```console.log``` statement will return an error.
7. On line 14, the console.log will print ```150```. This ```console.log``` will not cause an error because the *finalPrice* variable is declared at the top of the function, outside the for loop. Hence, when called, the variable exists in the scope and its value can be accessed.
8. Similar logic to question #4, the function will return the variable *discounted*. There will be no error in this function return statement. The return statement is simply returning the variable from the function. Since the discounted variable was declared within the scope of the function, there will be no error in returning its value. The function will return the following:
   1. ```discounted = [50, 100, 150]```
9. In a similar fashion/logic to question #5, line 11 will raise an error because we are trying to access a variable outside of its scope. Hence, when trying to access a variable that would be considered "does not exists", an error will arrise.
10. Line 12 will print "3". This is because the length variable is called outside the for loop and can be accessed anywhere in the function. Hence, no error will occur when running this line of code.
11. In a similar fashion as questions #4 and #8, the return value will be variable *discounted*. There will be no error in this function return statement. The return statement is simply returning a variable from the function. Since the discounted variable was declared within the scope of the function, there will be no error in returning its value. The function will return the following:
    1. ```discounted = [50, 100, 150]```
---

```javascript
let student = {
    name: 'Sarah',
    major: 'Computer Science',
    'Grad Year': '2022',
    greeting: function() {console.log('Hello!');},
    'Favorite Teacher': {
        name: 'Thomas Powell',
        course: 'CSE 110'
    },
    courseLoad: ['CSE 110', 'CSE 134', 'VIS 41']
};
```
12.  Notations:
     1.   ```student.name```
     2.   ```student['Grad Year']```
     3.   ```student.greeting()```
     4.   ```student['Favorite Teacher'].name```
     5.   ```student.courseLoad[0]```
---
13.  Arithmetic
     1.   "32" - string concatenation
     2.   1 - string is converted into number
     3.   3 - null is coerced to 0
     4.   '3null' - null is coerced to string
     5.   1 - true coerced to number (1)
     6.   0 - false and null coerced to 0
     7.   '3undefined' - undefined is coerced to a string
     8.   NaN = undefined is coerced to NaN
14.  Comparison
     1.   True - 2 is coerced to a number
     2.   False - '2' > '1', hence false
     3.   True - '2' is coerced into a number
     4.   False - '2' and 2 are not of the same datatype nor value
     5.   False - true is 1 is numeric value
     6.   True - Boolean() converts argument corresponding boolean value whether a non-zero element exists
15.  The difference between the ```==``` and the ```===``` operator is that ```==``` loosely checks whether two values are the same when one variable is coerced to another. ```===``` on the other hand checks for strict equality. Meaning it checks datatype and value, if the arguements are not of the same type, then false is immediately returned.
16.  [Link to File](/expose/javascript/part2-question16.js)
---
```javascript   
function modifyArray(array, callback) {
    const newArr = [];
    for (let i = 0; i < array.length; i++) {
        newArr.push(callback(array[i]));
    }
    return newArr;
}

function doSomething(num) {
    return num * 2;
}

modifyArray([1,2,3], doSomething);
```
17.  The result of the line `modifyArray([1,2,3], doSomething)` will result in ```[2,4,6]```. The code retusrns this ouput because in the initial function call ```modifyArray```, we pass in an array of integers and a callback (doSomething). Inside the function, we instantiate an array, ```newArr```, in which we later return. Prior to the return statement, we iterate over the array passed to the function and for each element, call on ```callback``` function which returns the argument passed in * 2. We then push this new value into the array ```newArr``` repeating this process over all elements in the array. Then at the end of the function, we return ```newArr```.
---
```javascript
let d = new Date();
let time = d.toLocalTimeString();
console.log(time);
``` 
18. [Link to File](/expose/javascript/part2-question18.js) 
```javascript
function printNums() {
    console.log(1);
    setTimeout(function() {console.log(2);}, 1000);
    setTimeout(function() {console.log(3);}, 0);
    console.log(4);
}

printNums();
```
19. The output of the code will be:
    - 1
    - 4
    - 3
    - 2