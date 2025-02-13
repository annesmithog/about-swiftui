# ZStack

```swift
let colors: [Color] = [.red, .green, .blue, .yellow, .pink]
var body: some View {
    ZStack {
        ForEach(0..<5) {
            Rectangle()
                .fill(colors[$0])
                .frame(width: 100, height: 100)
                .offset(x: CGFloat($0) * 10.0, y: CGFloat($0) * 10.0)
        }
    }
}
```
