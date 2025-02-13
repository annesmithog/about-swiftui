# Stepper

```swift
@State private var value: Int = 0
let step = 1
let range = 0...100
var body: some View {
    Stepper(
        value: $value,
        in: range,
        step: step
    ) {
        Text("Value: \(value) [\(range.description)]")
    }
    .padding(10)
}
```

<img src="/Images/View/Stepper1.png">
