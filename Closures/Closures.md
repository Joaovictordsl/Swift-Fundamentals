#Closures

## Closures are functions without a name (Anonymous)

They are self contained package of functionality that we can pass around and use.

Below is the way we normally use a function:
```
func functionName (parameter: parameterType) -> returnType {
  return output
}
```
An interesting thing is that we can actually pass a function as an input to another function
and use a function as an output of another function: 

```
func calculator(n1: Int, n2: Int, operation: (Int, Int) -> Int) -> Int {
    return operation(n1, n2)
}
func add(num1: Int, num2: Int) -> Int {
    return num1 + num2
}
print(calculator(n1: 1, n2: 2, operation: add))
```
To use a closure you have to:
  1. remove "func" word and the name of the function;
  2. put the curly bracket at the begining of the closure
  3. put the word "in" after the parameter

In general will look like:
```
{(parameters) -> return Type in
  statements
}
```

That being said, the example will look like this:
```
//Declaring a variable equal to the closure
let result = {(num1: Int, num2: Int) -> Int in return num1 + num2}

print(calculator(n1: 1, n2: 2, operation: result))
```

But, with closures we can simplify the code, like removing the type of the variables and the return type:
```
print(calculator(n1: 1, n2: 2, operation: { n1, n2 in n1 + n2}))
```
