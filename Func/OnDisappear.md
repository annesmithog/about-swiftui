<div style="font-size: 0.8rem;">

# onDisappear

ビューが消えた後に実行するアクションを追加する

```swift
Text("Hello")
    .onDisappear() { print("Helloと表示されていました。") }

Text("World")
    .onDisappear(perform: { print("Worldと表示されていました。") })
```

</div>
