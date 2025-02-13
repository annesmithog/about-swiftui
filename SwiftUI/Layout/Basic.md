<div style="font-size: 0.8rem;">

# レイアウトの基本情報

## HStack

サブビューを水平方向に並べる

```swift
HStack {
    Text("A")
    Text("B")
}
```

## VStack

サブビューを垂直方向に並べる

```swift
VStack {
    Text("A")
    Text("B")
}
```

## ZStack

サブビューを重ねて並べる

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

## Grid

他のビューを２次元レイアウトに配置する

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

<img src="/Images/Layout/Grid1.png">

## Spacer

柔軟なスペース

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

<img src="/Images/Layout/Spacer1.png">

</div>
