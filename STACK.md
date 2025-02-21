# スタック

#### HStack

```swift
HStack {
    Text("A")
    Text("B")
}
```

#### VStack

```swift
VStack {
    Text("A")
    Text("B")
}
```

#### ZStack

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

#### Grid

```swift
// 基本
Grid {
    GridRow {
        Text("Fire")
        Image(systemName: "flame")
    }
    GridRow {
        Image(systemName: "bolt")
        Text("Bolt")
    }
}
// 列数
Grid(alignment: .bottom, horizontalSpacing: 1, verticalSpacing: 30) {
    GridRow {
        Text("Row 1")
        ForEach(0..<2) { _ in Color.red }
    }
    GridRow {
        Text("Row 2")
        ForEach(0..<4) { _ in Color.green }
    }
}.frame(height: 100)
```

<img src="/images/stack/grid.png">

#### Spacer

```swift
let name: String = "Anne Smith"
    
var body: some View {
    HStack {
        Image(systemName: "person")
        Text(name)
    }
    .border(.blue)
    
    HStack {
        Spacer()
        Image(systemName: "person")
        Text(name)
    }
    .border(.green)
    
    HStack {
        Image(systemName: "person")
        Text(name)
        Spacer()
    }
    .border(.red)
}
```

<img src="/images/stack/spacer.png">
