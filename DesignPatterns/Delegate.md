<h1>Delegate Design Pattern</h1>

<h2>It enables a class or structure to delegate some of its responsibilities to another instance, often referred to as a "delegate."</h2>

In the delegate pattern, two objects are involved: the delegating object and the delegate. The delegating object contains a reference to the delegate, and it calls methods on the delegate to notify it of certain events or to request specific actions. This allows for a clean separation of concerns and promotes modularity in the codebase.

<h2>Protocol Definition:</h2>

Define a protocol that declares the methods that the delegate can implement. This protocol serves as a contract, specifying the behavior that the delegate must adhere to.
```
protocol MyDelegate: class {
    func didReceiveData(data: String)
    func didFailWithError(error: Error)
}
```
