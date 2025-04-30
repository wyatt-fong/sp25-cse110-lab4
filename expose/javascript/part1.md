## Part 1
1. On line 9, the ```console.log('values added: ', result)``` prints:
   1. "values added: 20"
2. On line 13, the ```console.log('final result: ', result);``` prints:
   1. "final result: 20"
3. We should not use ```var``` because it can lead to scope issues within the file, lead to bugs and unexpected behaviors. If ```var``` is used, then we would need to worry about the "globalness" of the variable and accidentally changing its value when unintended. Essentially, using ```var``` instead of ```let``` and ```const``` would create fake global variables that could potentially wreack havoc into our code.

4. On line 9, the ```console.log('values added: ", result);``` prints:
   1. "values added: 20'
5. On line 13, an error occurs because code are trying to access a variable that it does not have access to. The variable result is declared with the keyword ```let``` and thus only exists in the scope of the if statement. Outside the if statement, there does not exist a variable named let and will therefore result in an error if called.
6. The code will return an error before line 9 will be able to be executed due to an attempt at assigning a value outside of its initial decleration. A const variable's value cannot be changed post declaration. Hence, when line 8 tries to reassign the constant variable, an error arrises.
7. Similar logic/answer as question #6.
