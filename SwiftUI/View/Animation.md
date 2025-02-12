<div style="font-size: 0.8rem;">

# アニメーション

## はじめてのアニメーション

```swift
@State private var isLarge: Bool = false
var body: some View {
    Button {
        isLarge.toggle()
    } label: {
        Circle()
            .frame(width: 100, height: 100)
            .scaleEffect(isLarge ? 3 : 1)
            .animation(.spring(), value: isLarge)
    }
}
```

<video width="320" height="240" controls>
    <source src="/Movies/View/AnimationExample.mov" type="video/mp4">
</video>

</div>