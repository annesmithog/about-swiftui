<div style="font-size: 0.8rem;">

# Button

## 基本

##### 簡単なボタン

```swift
Button("Tap Me", action: { print("Tapped.") })
```

##### 関数化

```swift
var body: some View {
    VStack {
        btn1()
    }
}

fileprivate func btn1() -> Button<Text> {
    Button(action: {
        print("Tapped.")
    }) {
        Text("Tap Me.")
    }
}
```

##### カウンター

```swift
struct ContentView: View {
    @State var count = 0
    var body: some View {
        VStack {
            Button(action: {
                count += 1
            }) {
                Text("Tap Count")
                Text(String(count))
            }
        }
    }
}
```

<img src="/Images/Button/ButtonCounter.png">

##### リストに表示

```swift
List {
    Button(action: { print("1 Clicked.") }) { Text("One") }
    Button(action: { print("2 Clicked.") }) { Text("Two") }
    Button(action: { print("3 Clicked.") }) { Text("Three") }
}
```

<img src="/Images/Button/ButtonList.png">

##### 役割の割り当て

```swift
// 操作をキャンセルするボタンを示す
Button("Cancel", role: .cancel, action: { print("Cancel") })
// 破壊的なボタンを示す
Button("Delete", role: .destructive, action: { print("Delete") })
```

<img src="/Image/ButtonRole.png">

##### 外観のカスタマイズ

```swift
HStack {
    Button("Sign In", action: { print("Sign In!") })
    Button("Register", action: { print("Register!") })
}
.buttonStyle(.bordered)
```

<img src="/Images/Button/ButtonStyle.png">

## ボタンの作成

##### `.buttonStyle` - スタイルの変更

```swift
VStack {
    Button("Button 1", action: {}).buttonStyle(.automatic)
    Button("Button 2", action: {}).buttonStyle(.bordered)
    Button("Button 3", action: {}).buttonStyle(.borderedProminent)
    Button("Button 4", action: {}).buttonStyle(.borderless)
    Button("Button 5", action: {}).buttonStyle(.plain)
}
```

<img src="/Images/Button/ButtonStyles.png">

</div>
