## Grid

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
