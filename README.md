# Passing-arguments-

var obj = {a: 2};
function myfunc(arg){
 arg = {a: 5}; // Note the assignment is to the parameter variable itself
}
myfunc(obj);
console.log(obj.a); // 2
However, changes made to (nested) properties of such arguments, will be visible to the caller:
var obj = {a: 2};
function myfunc(arg){
 arg.a = 5; // assignment to a property of the argument
}
myfunc(obj);
console.log(obj.a); // 5
