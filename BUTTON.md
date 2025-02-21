# ボタン

#### Button

```swift
// 基本
Button(action: { print("Button 1 clicked") }) {
    Text("Button 1")
}
// Label使用 1
Button(action: {} ) {
    Label("Button 2", systemImage: "person.fill")
}
// Label使用 2
Button("Button 3", systemImage: "person", action: {} )
// labelStyle適用
Button("Button 4", systemImage: "flame", action: {} )
    .labelStyle(.iconOnly)
// 役割の割り当て
Button("Button 5", role: .destructive, action: {})
// スタイル設定
Button("Sign In", action: {}).buttonStyle(.borderedProminent)
Button("Register", action: {}).buttonStyle(.bordered)
```

<img src="/images/button/button1.png">



