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

##### `.linear`

![demo](https://github.com/annesmithog/about-swiftui/blob/main/Videos/View/AnimationExample.gif?raw=true)

##### `.default`
##### `.easeInOut`
##### `.easeIn`
##### `.easeOut`

</div>
