# `.contextMenu`

```swift
Text("console.log('Hello')")
    .padding()
    .contextMenu {
        Button {
            
        } label: {
            Label("Copy", systemImage: "document.on.document")
        }
        Button {
            
        } label: {
            Text("X")
        }
    }
```

<img src="/Images/View/ContextMenu1.png">
