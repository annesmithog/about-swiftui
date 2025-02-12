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

![demo](https://raw.github.com/wiki/annesmithog/Projects/about-swiftui/Videos/View/AnimationExample.gif)

![demo](https://github.com/wiki/annesmithog/about-swiftui/videos/AnimationExample.gif)

<!-- <video width="320" height="240" controls>
    <source src="/Movies/View/AnimationExample.gif" type="video/mp4">
</video> -->

</div>