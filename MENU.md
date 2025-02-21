# メニュー

#### Menu

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

<img src="/images/menu/menu.png">

#### contextMenu

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

<img src="/images/menu/contextmenu.png">
