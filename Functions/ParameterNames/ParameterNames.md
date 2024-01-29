<h1>Parameter Names</h1>

<h2>Swift has the ability to have completely seperate internal and external parameter names</h2>

Looks something like this:
```
func myFunc(external internal: Type) {
  print(internal)
}
```

Defining the Function:
```
func myFunc(name eman: Type) {
  print(eman)
}
```
 Calling the Function:
```
myFunc(name: value)
```

The external P. Name is what we use when we call the function.
```
myFunc(external: value)
```

The internal P. Name is what we use when we need to use the value of the parameter within the function.
```
print(internal)
```

So, you can actually omit the external parameter name, just passing the value.
You have to turn the external P. Name to an Underscore:
```
func myFunc(_ eman: Type) {
  print(eman)
}

myFunc(value)
```

<h2>Example:</h2>

```
func add(_ num1: Int, _ num2: Int) -> Int {
    let result = num1 + num2
    return result
}

print(add(1,2))
```





