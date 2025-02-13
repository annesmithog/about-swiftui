# AsyncImage

```swift
var cover = "https://img.hmv.co.jp/image/jacket/400/06/9/0/767.jpg"

AsyncImage(url: URL(string: cover)) { image in
    // 読み込まれたら色々やる
    image
        .resizable()
        .scaledToFit()
        .cornerRadius(30)
} placeholder: {
    // 読み込まれない間、ローディングアニメーション
    ProgressView()
}
.frame(width: 300, height: 300)
```

<img src="/Images/View/ImageAsync.png">
