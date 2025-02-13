# Toggle

```swift
@State private var isOn = false
var body: some View {
    
    Toggle(isOn: $isOn) {
        Text("Toggle 1")
    }
    
    Toggle(
        "Toggle 2",
        systemImage: "person",
        isOn: $isOn
    )
    
    Toggle("Toggle 3", isOn: $isOn)
    
    Toggle(isOn: $isOn) {
        Text("Toggle 4-1")
        Text("Toggle 4-2")
    }
    
    Toggle("Toggle 5", isOn: $isOn).toggleStyle(.button)
}
```

<img src="/Images/View/Toggle1.png">
