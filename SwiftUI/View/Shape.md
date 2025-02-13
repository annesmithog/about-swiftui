<div style="font-size: 0.8rem;">

# 形状

## 長方形

```swift
VStack {
    // 長方形
    Rectangle()
        .frame(width: 200, height: 100)
    // 角が丸い長方形
    RoundedRectangle(cornerRadius: .infinity)
        .frame(width: 200, height: 100)
}
```

## 円形

```swift
VStack {
    // 円
    Circle()
        .frame(height: 100)
    // 楕円
    Ellipse()
        .frame(height: 100)
    // カプセル
    Capsule()
        .frame(height: 100)
}
```

</div>
