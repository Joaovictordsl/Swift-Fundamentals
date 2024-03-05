# MVVM Pattern in SwiftUI with Swift

## Overview

MVVM (Model-View-ViewModel) is a design pattern commonly used in iOS development to separate concerns and create modular testable and maintainable code.

## Components

### Model
- Represents the data and business logic of the application.
- Independent of the user interface.
- Example: 

```swift
struct Person {
    let name: String
    let age: Int
}
```

### ViewModel
- Acts as an intermediary between the Model and the View.
- Provides data from the Model to the View and handles user interactions.
- Contains presentation logic and state management.
- Example:

```swift
class PersonViewModel: ObservableObject {
    @Published var person: Person
    
    init(person: Person) {
        self.person = person
    }
    
    var name: String {
        return person.name
    }
    
    var ageText: String {
        return "Age: \(person.age)"
    }
}
```

### View
- Represents the user interface elements.
- Displays data to the user and sends user actions to the ViewModel.
- Example:

```swift
struct PersonView: View {
    @ObservedObject var personViewModel: PersonViewModel
    
    var body: some View {
        VStack {
            Text(personViewModel.name)
            Text(personViewModel.ageText)
        }
    }
}
```

## Usage

```swift
let person = Person(name: "Sponge Bob", age: 30)
let viewModel = PersonViewModel(person: person)
let view = PersonView(personViewModel: viewModel)
```
