# Menu

```swift
Menu("Actions") {
    Button("Duplicate", action: {})
    Button("Rename", action: {})
    Button("Delete", action: {})
    Menu("Copy") {
        Button("Copy 1", action: {})
        Button("Copy 2", action: {})
    }
    .padding(.top)
}
```

<img src="/Images/View/Menu1.png">
