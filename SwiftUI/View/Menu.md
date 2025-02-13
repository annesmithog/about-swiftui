<div style="font-size: 0.8rem;">

# メニューとコマンド

## Menu

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

[Menu Style](/SwiftUI/View/ViewStyle.md#menustyle)

<img src="/Images/View/Menu1.png">

## `.contextMenu`

長押ししたら出るやつ

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

</div>
