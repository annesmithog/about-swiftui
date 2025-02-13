<div style="font-size: 0.8rem;">

# onAppear

ビューが表示される前に実行するアクションを追加する

```swift
Text("Hello")
    .onAppear() { print("Helloが表示されました。") }

Text("World")
    .onAppear(perform: { print("Worldが表示されました。") })
```

</div>
