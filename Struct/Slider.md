# Slider

```swift
@State private var score: Double = 6.0
@State private var isEditing: Bool = false
var body: some View {
    VStack {
        Slider(
            value: $score,
            in: 0...10,
            step: 0.1,
            onEditingChanged: { editing in
                isEditing = editing
            }
        )
        Text("\(score)").foregroundColor(isEditing ? .red : .blue)
    }
}
```

<img src="/Images/View/Slider1.png">
