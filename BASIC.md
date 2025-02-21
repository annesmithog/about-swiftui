# 基本

#### View

```swift
struct ContentView: View {
    var body: some View {
        Text("Hello, World!")
    }
}
```

#### Text

```swift
Text("Hello")
```

#### Label

```swift
Label("Lightning", systemImage: "bolt.fill")
```

#### TextField

```swift
@State private var username: String = ""
var body: some View {
    TextField("Username", text: $username)
}
```

#### SecureField

```swift
@State private var password: String = ""
var body: some View {
    SecureField("Password", text: $password)
}
```





