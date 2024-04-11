## Swift Basics

#### 1. Optional

<details> 
  <summary>Solution</summary>

An `Optional` is a type that can hold either a value or `nil`. For example, `String?` is an optional string, which means it can either hold a `String` value or `nil`.

</details>

#### 2. Optional Binding

<details> 
  <summary>Solution</summary>

Optional binding is a way to safely unwrap an optional. It checks whether an optional contains a value, and if so, makes that value available as a temporary constant or variable. For example:

```swift
if let unwrappedString = someOptionalString {
    print(unwrappedString) // Safe access to the value
}
```

</details>

#### 3. Forced Unwrapping

<details> 
  <summary>Solution</summary>

Forced unwrapping is a way to access the underlying value of an optional. If the optional is `nil`, a runtime error will occur. For example:

```swift
let unwrappedString = someOptionalString! // Unsafe and can crash if someOptionalString is nil
```

</details>

#### 4. Nil Coalescing Operator (??)

<details> 
  <summary>Solution</summary>

The nil coalescing operator `??` is used to provide a default value for an optional. If the optional contains a value, it is unwrapped; otherwise, the default value is used. For example:

```swift
let string = someOptionalString ?? "Default String"
```

</details>
